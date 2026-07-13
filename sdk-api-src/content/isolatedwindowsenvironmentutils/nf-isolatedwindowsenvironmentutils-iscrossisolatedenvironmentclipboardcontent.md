---
UID: NF:isolatedwindowsenvironmentutils.IsCrossIsolatedEnvironmentClipboardContent
tech.root: security
title: IsCrossIsolatedEnvironmentClipboardContent
ms.date: 03/09/2023
targetos: Windows
description: IsCrossIsolatedEnvironmentClipboardContent is called after an app detects a paste failure to determine if the content being pasted came from the other side of a Microsoft Defender Application Guard (MDAG) boundary.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: isolatedwindowsenvironmentutils.dll
req.header: isolatedwindowsenvironmentutils.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: IsolatedWindowsEnvironmentUtils.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - isolatedwindowsenvironmentutils.dll
api_name:
 - IsCrossIsolatedEnvironmentClipboardContent
f1_keywords:
 - IsCrossIsolatedEnvironmentClipboardContent
 - isolatedwindowsenvironmentutils/IsCrossIsolatedEnvironmentClipboardContent
dev_langs:
 - c++
helpviewer_keywords:
 - IsCrossIsolatedEnvironmentClipboardContent
---

## -description

**IsCrossIsolatedEnvironmentClipboardContent** can be called after an app detects a paste failure to determine if the content being pasted came from the other side of a [Microsoft Defender Application Guard (MDAG)](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview) boundary. In this scenario, applications can display a custom error message to help users understand that the clipboard operation was intentionally blocked by MDAG.

## -parameters

### -param isCrossIsolatedEnvironmentClipboardContent

`[out]`

A pointer to a boolean value that receives the result of the API. This parameter will be `true` if the clipboard content came from the other side of a MDAG boundary, `false` otherwise.

## -returns

If the function succeeds, the return value is `S_OK`. If it fails, it returns an `HRESULT` error code.

## -remarks

This API can be called from both the host and Isolated Windows Environment app instance and can detect both relevant scenarios:

- Scenario 1 -  Called from a host document (ex: pasting content to the host)
  - Returns true if the clipboard content came from any Isolated Windows Environment.
- Scenario 2 -  Called from an Isolated Windows Environment document (ex: pasting content to Isolated Environment)
  - Returns true if the clipboard content came from the host, or from a different Isolated Windows Environment.

This API also allows apps to continue to show their default paste error handler where appropriate. For example, copy/pasting content within the same Isolated Environment is not subject to MDAG clipboard policy. Any failure would be due to an unrelated paste error, such as corrupted data. In this case, **IsCrossIsolatedEnvironmentClipboardContent** would return false, so the app knows to follow their default paste error handler flow.

#### Examples

This sample shows how an app can customize the paste error message shown to the user. The first snippet shows how to use **IsCrossIsolatedEnvironmentClipboardContent** to show an appropriate error message if an app’s paste handler fails. In this sample, the app’s paste handler `OnPaste` (defined in the second code snippet) is invoked by the `WM_PASTE` message received in its `WndProc`.

```cpp
// Assume this is the WndProc method that handles WM messages for an app.
// Assume SampleAppHelperClass::DisplayMsgBox shows a simple UI error dialog with given string.

LRESULT CALLBACK SampleAppWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
  LRESULT retVal = 0;
  switch (message)
  {
  case WM_PASTE:
  {
    RETURN_LAST_ERROR_IF(!OpenClipboard(hWnd));

    // See definition of OnPaste in code snippet #2, below.
    retVal = OnPaste(hWnd, message, wParam, lParam);

    // To avoid a race condition with the clipboard changing underneath us, call
    // IsCrossIsolatedEnvironmentClipboardContent with the clipboard still open.
    HRESULT hr = S_OK;
    BOOL isCrossEnvContent = FALSE;

    hr = IsCrossIsolatedEnvironmentClipboardContent(&isCrossEnvContent);

    CloseClipboard();

    if (retVal != ERROR_SUCCESS)
    {
      // Show a MDAG specific error message if the clipboard content crossed the host/isolated
      // environment boundary. Otherwise, show the app’s default paste error message.
      if (SUCCEEDED(hr) && isCrossEnvContent)
      {
        // This runs on both the host and Isolated Environment app instance, so customize error
        // message per scenario.
        BOOL isIsolatedWindowsEnvironment = FALSE;
        IsProcessInIsolatedWindowsEnvironment(&isIsolatedWindowsEnvironment);
        std::wstring direction = isIsolatedWindowsEnvironment ? L"into" : L"from";

        SampleAppHelperClass::DisplayMsgBox(hWnd, L"Pasting content %s a MDAG document failed, verify this operation is permitted by your administrator.\n", direction.c_str());
      }
      else
      {
        SampleAppHelperClass::DisplayMsgBox(hWnd, L"Paste operation failed.\nError code 0x%x", retVal);
      }
    }
  }
  break;
  default:
    return DefWindowProc(hWnd, message, wParam, lParam);
  }
  return retVal;
}
```

The second code snippet shows an app’s paste handler to demonstrate how clipboard actions may fail if blocked by MDAG.

```cpp
// Invoked by user Paste action, such as Ctr+V or clicking the Paste button.
HRESULT OnPaste(HWND hWnd)
{
  RETURN_LAST_ERROR_IF(!IsClipboardFormatAvailable(CF_TEXT));
  HGLOBAL clipboardData = GetClipboardData(CF_TEXT);
  RETURN_LAST_ERROR_IF(clipboardData == NULL);

  // Now that we've verified clipboard access suceeds, assume InsertTextFromClipboard is an
  // application defined method to insert text into desired location.
  RETURN_IF_FAILED(InsertTextFromClipboard(clipboardData, hWnd));

  CloseClipboard();

  return S_OK;
}
```

## -see-also

[Microsoft Defender Application Guard overview](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview)

[IsolatedWindowsEnvironment](/uwp/api/windows.security.isolation.isolatedwindowsenvironment)

[IsolatedWindowsEnvironmentHost](/uwp/api/windows.security.isolation.isolatedwindowsenvironmenthost)
