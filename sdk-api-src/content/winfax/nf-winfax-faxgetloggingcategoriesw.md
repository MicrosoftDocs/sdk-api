---
UID: NF:winfax.FaxGetLoggingCategoriesW
title: FaxGetLoggingCategoriesW function (winfax.h)
description: The FaxGetLoggingCategories function returns to a fax client application the current logging categories for the fax server to which the client has connected. (Unicode)
helpviewer_keywords: ["FaxGetLoggingCategories", "FaxGetLoggingCategories function [Fax Service]", "FaxGetLoggingCategoriesW", "_mfax_faxgetloggingcategories", "fax._mfax_faxgetloggingcategories", "winfax/FaxGetLoggingCategories", "winfax/FaxGetLoggingCategoriesW"]
old-location: fax\_mfax_faxgetloggingcategories.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6cab.htm
ms.date: 12/05/2018
ms.keywords: FaxGetLoggingCategories, FaxGetLoggingCategories function [Fax Service], FaxGetLoggingCategoriesA, FaxGetLoggingCategoriesW, _mfax_faxgetloggingcategories, fax._mfax_faxgetloggingcategories, winfax/FaxGetLoggingCategories, winfax/FaxGetLoggingCategoriesA, winfax/FaxGetLoggingCategoriesW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxGetLoggingCategoriesW (Unicode) and FaxGetLoggingCategoriesA (ANSI)
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
 - FaxGetLoggingCategoriesW
 - winfax/FaxGetLoggingCategoriesW
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
 - FaxGetLoggingCategories
 - FaxGetLoggingCategoriesA
 - FaxGetLoggingCategoriesW
---

# FaxGetLoggingCategoriesW function


## -description

The <b>FaxGetLoggingCategories</b> function returns to a fax client application the current logging categories for the fax server to which the client has connected. A logging category determines the errors or other events the fax server records in the application event log.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param Categories [out]

Type: <b>PFAX_LOG_CATEGORY*</b>

Pointer to the address of a buffer to receive an array of <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a> structures. Each structure describes one current logging category. The data includes the descriptive name of the logging category, the category number, and the current logging level. 

                    

For a description of predefined logging categories and logging levels, see the <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a> topic. For information about memory allocation, see the following Remarks section.

### -param NumberCategories [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a> structures the function returns in the <i>Categories</i> parameter.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_CONFIG_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>Categories</i>, <i>NumberCategories</i>, or <i>FaxHandle</i> parameters are <b>NULL</b>.

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

A fax client application typically calls the <b>FaxGetLoggingCategories</b> function to query the current logging categories and logging levels for a fax server. To modify the current logging categories and levels, call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetloggingcategoriesa">FaxSetLoggingCategories</a> function.

The <b>FaxGetLoggingCategories</b> function allocates the memory required for the <a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a> buffer array pointed to by the <i>Categories</i> parameter. An application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-logging-categories">Managing Logging Categories</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.





> [!NOTE]
> The winfax.h header defines FaxGetLoggingCategories as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_log_categorya">FAX_LOG_CATEGORY</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetloggingcategoriesa">FaxSetLoggingCategories</a>
