---
UID: NF:wininet.InternetConfirmZoneCrossingA
title: InternetConfirmZoneCrossingA function (wininet.h)
description: Checks for changes between secure and nonsecure URLs. Always inform the user when a change occurs in security between two URLs. Typically, an application should allow the user to acknowledge the change through interaction with a dialog box. (InternetConfirmZoneCrossingA)
helpviewer_keywords: ["InternetConfirmZoneCrossingA", "wininet/InternetConfirmZoneCrossingA"]
old-location: wininet\internetconfirmzonecrossing.htm
tech.root: wininet
ms.assetid: e14f58df-5457-4a17-919c-6a25691c2ee1
ms.date: 12/05/2018
ms.keywords: InternetConfirmZoneCrossing, InternetConfirmZoneCrossing function [WinINet], InternetConfirmZoneCrossingA, InternetConfirmZoneCrossingW, _inet_internetconfirmzonecrossing_function, wininet.internetconfirmzonecrossing, wininet/InternetConfirmZoneCrossing, wininet/InternetConfirmZoneCrossingA, wininet/InternetConfirmZoneCrossingW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetConfirmZoneCrossingW (Unicode) and InternetConfirmZoneCrossingA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetConfirmZoneCrossingA
 - wininet/InternetConfirmZoneCrossingA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetConfirmZoneCrossing
 - InternetConfirmZoneCrossingA
 - InternetConfirmZoneCrossingW
---

# InternetConfirmZoneCrossingA function


## -description

Checks for changes between secure and nonsecure URLs. Always inform the user when a change occurs in security between two URLs. Typically, an application should allow the user to acknowledge the change through interaction with a dialog box.

## -parameters

### -param hWnd [in]

Handle to the parent window for any required dialog box.

### -param szUrlPrev [in]

Pointer to a null-terminated string that specifies the URL that was viewed before the current request was made.

### -param szUrlNew [in]

Pointer to a null-terminated string that specifies the new URL that the user has requested to view.

### -param bPost [in]

Not implemented.

## -returns

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The user confirmed that it was okay to continue, or there was no user input required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to carry out the request.

</td>
</tr>
</table>

## -remarks

 Always inform the user when a change in security level occurs, or you risk subjecting the user to  involuntary information disclosure.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetConfirmZoneCrossing as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/enabling-internet-functionality">Enabling Internet Functionality</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
