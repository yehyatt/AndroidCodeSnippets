# AndroidCodeSnippets
Code Snippets of android

progress = ProgressDialog.show(this, "dialog title",
  "dialog message", true);

new Thread(new Runnable() {
  @Override
  public void run()
  {
    // do the thing that takes a long time

    runOnUiThread(new Runnable() {
      @Override
      public void run()
      {
        progress.dismiss();
      }
    });
  }
}).start();
