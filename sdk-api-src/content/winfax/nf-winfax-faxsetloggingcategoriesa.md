---
UID: NF:winfax.FaxSetLoggingCategoriesA
title: FaxSetLoggingCategoriesA function
author: windows-sdk-content
description: A fax client application calls the FaxSetLoggingCategories function to modify the current logging categories for the fax server to which the client has connected.
old-location: fax\_mfax_faxsetloggingcategories.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_30vn.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxSetLoggingCategories, FaxSetLoggingCategories function [Fax Service], FaxSetLoggingCategoriesA, FaxSetLoggingCategoriesW, _mfax_faxsetloggingcategories, fax._mfax_faxsetloggingcategories, winfax/FaxSetLoggingCategories, winfax/FaxSetLoggingCategoriesA, winfax/FaxSetLoggingCategoriesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxSetLoggingCategoriesA function


## -description


A fax client application calls the <b>FaxSetLoggingCategories</b> function to modify the current logging categories for the fax server to which the client has connected. A logging category determines the errors or other events the fax server records in the application event log.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param Categories [in]

Type: <b>const <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a> structures. Each structure contains the data to modify one logging category. The data includes the descriptive name of the logging category, the category number, and the current logging level for the category. For a description of predefined logging categories and logging levels, see the <b>FAX_LOG_CATEGORY</b> topic.


### -param NumberCategories [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that contains the number of <a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a> structures the function passes in the <i>Categories</i> parameter.


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
The <i>FaxHandle</i> parameter is <b>NULL</b>; or the <i>hWnd</i> parameter is specified but the <i>FaxHandle</i> parameter does not specify a connection with a local fax server; or the <i>MessageStart</i> parameter specifies a message in the range below <a href="_win32_WM_USER">WM_USER</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_CONFIG_SET</a> access is required.

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



The fax service administration application, a Microsoft Management Console (MMC) snap-in component, typically calls the <b>FaxSetLoggingCategories</b> function to modify the current logging categories and logging levels for a fax server. To query the categories and levels, an application can call the <a href="https://msdn.microsoft.com/bcd650b3-92f3-4b3b-b4c2-c3418f914711">FaxGetLoggingCategories</a> function. For more information, see <a href="https://msdn.microsoft.com/958fecf7-a787-4f86-bc67-53f7564ec43a">Managing Logging Categories</a>.




## -see-also




<a href="https://msdn.microsoft.com/125addbb-5567-4ddc-9d48-e05ae93ec075">FAX_LOG_CATEGORY</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/bcd650b3-92f3-4b3b-b4c2-c3418f914711">FaxGetLoggingCategories</a>
 

 

