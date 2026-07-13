---
UID: NF:winfax.FaxSetLoggingCategoriesW
title: FaxSetLoggingCategoriesW function (winfax.h)
description: A fax client application calls the FaxSetLoggingCategories function to modify the current logging categories for the fax server to which the client has connected. (Unicode)
helpviewer_keywords: ["FaxSetLoggingCategories", "FaxSetLoggingCategories function [Fax Service]", "FaxSetLoggingCategoriesW", "_mfax_faxsetloggingcategories", "fax._mfax_faxsetloggingcategories", "winfax/FaxSetLoggingCategories", "winfax/FaxSetLoggingCategoriesW"]
old-location: fax\_mfax_faxsetloggingcategories.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_30vn.htm
ms.date: 12/05/2018
ms.keywords: FaxSetLoggingCategories, FaxSetLoggingCategories function [Fax Service], FaxSetLoggingCategoriesA, FaxSetLoggingCategoriesW, _mfax_faxsetloggingcategories, fax._mfax_faxsetloggingcategories, winfax/FaxSetLoggingCategories, winfax/FaxSetLoggingCategoriesA, winfax/FaxSetLoggingCategoriesW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetLoggingCategoriesW (Unicode) and FaxSetLoggingCategoriesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxSetLoggingCategoriesW
 - winfax/FaxSetLoggingCategoriesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxSetLoggingCategories
 - FaxSetLoggingCategoriesA
 - FaxSetLoggingCategoriesW
---

# FaxSetLoggingCategoriesW function


## -description

A fax client application calls the <b>FaxSetLoggingCategories</b> function to modify the current logging categories for the fax server to which the client has connected. A logging category determines the errors or other events the fax server records in the application event log.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param Categories [in]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a>*</b>

Pointer to an array of <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a> structures. Each structure contains the data to modify one logging category. The data includes the descriptive name of the logging category, the category number, and the current logging level for the category. For a description of predefined logging categories and logging levels, see the <b>FAX_LOG_CATEGORY</b> topic.

### -param NumberCategories [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that contains the number of <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a> structures the function passes in the <i>Categories</i> parameter.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>FaxHandle</i>, <i>Categories</i>, or <i>NumberCategories</i> parameters are invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is <b>NULL</b>; or the <i>hWnd</i> parameter is specified but the <i>FaxHandle</i> parameter does not specify a connection with a local fax server; or the <i>MessageStart</i> parameter specifies a message in the range below <a href="/windows/desktop/winmsg/wm-user">WM_USER</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_CONFIG_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
</table>

## -remarks

The fax service administration application, a Microsoft Management Console (MMC) snap-in component, typically calls the <b>FaxSetLoggingCategories</b> function to modify the current logging categories and logging levels for a fax server. To query the categories and levels, an application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetloggingcategoriesa">FaxGetLoggingCategories</a> function. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-logging-categories">Managing Logging Categories</a>.





> [!NOTE]
> The winfax.h header defines FaxSetLoggingCategories as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetloggingcategoriesa">FaxGetLoggingCategories</a>
