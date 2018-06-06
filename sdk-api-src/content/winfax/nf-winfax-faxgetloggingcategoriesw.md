---
UID: NF:winfax.FaxGetLoggingCategoriesW
title: FaxGetLoggingCategoriesW function
author: windows-sdk-content
description: The FaxGetLoggingCategories function returns to a fax client application the current logging categories for the fax server to which the client has connected.
old-location: fax\_mfax_faxgetloggingcategories.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6cab.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FaxGetLoggingCategories, FaxGetLoggingCategories function [Fax Service], FaxGetLoggingCategoriesA, FaxGetLoggingCategoriesW, _mfax_faxgetloggingcategories, fax._mfax_faxgetloggingcategories, winfax/FaxGetLoggingCategories, winfax/FaxGetLoggingCategoriesA, winfax/FaxGetLoggingCategoriesW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
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
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxGetLoggingCategoriesW function


## -description


The <b>FaxGetLoggingCategories</b> function returns to a fax client application the current logging categories for the fax server to which the client has connected. A logging category determines the errors or other events the fax server records in the application event log.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param Categories [out]

Type: <b>PFAX_LOG_CATEGORY*</b>

Pointer to the address of a buffer to receive an array of <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a> structures. Each structure describes one current logging category. The data includes the descriptive name of the logging category, the category number, and the current logging level. 

                    

For a description of predefined logging categories and logging levels, see the <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a> topic. For information about memory allocation, see the following Remarks section.


### -param NumberCategories [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a> structures the function returns in the <i>Categories</i> parameter.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

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
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_CONFIG_QUERY</a> access is required.

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



A fax client application typically calls the <b>FaxGetLoggingCategories</b> function to query the current logging categories and logging levels for a fax server. To modify the current logging categories and levels, call the <a href="https://msdn.microsoft.com/4faddf91-a689-4247-86af-8d6dbc1b6af3">FaxSetLoggingCategories</a> function.

The <b>FaxGetLoggingCategories</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a> buffer array pointed to by the <i>Categories</i> parameter. An application must call the <a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/958fecf7-a787-4f86-bc67-53f7564ec43a">Managing Logging Categories</a> and <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/4faddf91-a689-4247-86af-8d6dbc1b6af3">FaxSetLoggingCategories</a>
 

 

