---
UID: NF:winfax.FaxGetLoggingCategoriesA
title: FaxGetLoggingCategoriesA function
author: windows-sdk-content
description: The FaxGetLoggingCategories function returns to a fax client application the current logging categories for the fax server to which the client has connected.
old-location: fax\_mfax_faxgetloggingcategories.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6cab.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: FaxGetLoggingCategories, FaxGetLoggingCategories function [Fax Service], FaxGetLoggingCategoriesA, FaxGetLoggingCategoriesW, _mfax_faxgetloggingcategories, fax._mfax_faxgetloggingcategories, winfax/FaxGetLoggingCategories, winfax/FaxGetLoggingCategoriesA, winfax/FaxGetLoggingCategoriesW
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
req.unicode-ansi: FaxGetLoggingCategoriesW (Unicode) and FaxGetLoggingCategoriesA (ANSI)
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
 - FaxGetLoggingCategories
 - FaxGetLoggingCategoriesA
 - FaxGetLoggingCategoriesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxGetLoggingCategoriesA function


## -description


The <b>FaxGetLoggingCategories</b> function returns to a fax client application the current logging categories for the fax server to which the client has connected. A logging category determines the errors or other events the fax server records in the application event log.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param Categories [out]

Type: <b>PFAX_LOG_CATEGORY*</b>

Pointer to the address of a buffer to receive an array of <a href="https://msdn.microsoft.com/en-us/library/ms690890(v=VS.85).aspx">FAX_LOG_CATEGORY</a> structures. Each structure describes one current logging category. The data includes the descriptive name of the logging category, the category number, and the current logging level. 

                    

For a description of predefined logging categories and logging levels, see the <a href="https://msdn.microsoft.com/en-us/library/ms690890(v=VS.85).aspx">FAX_LOG_CATEGORY</a> topic. For information about memory allocation, see the following Remarks section.


### -param NumberCategories [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://msdn.microsoft.com/en-us/library/ms690890(v=VS.85).aspx">FAX_LOG_CATEGORY</a> structures the function returns in the <i>Categories</i> parameter.


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
Access is denied. <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">FAX_CONFIG_QUERY</a> access is required.

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



A fax client application typically calls the <b>FaxGetLoggingCategories</b> function to query the current logging categories and logging levels for a fax server. To modify the current logging categories and levels, call the <a href="https://msdn.microsoft.com/en-us/library/ms691374(v=VS.85).aspx">FaxSetLoggingCategories</a> function.

The <b>FaxGetLoggingCategories</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/en-us/library/ms690890(v=VS.85).aspx">FAX_LOG_CATEGORY</a> buffer array pointed to by the <i>Categories</i> parameter. An application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690748(v=VS.85).aspx">Managing Logging Categories</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690890(v=VS.85).aspx">FAX_LOG_CATEGORY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691374(v=VS.85).aspx">FaxSetLoggingCategories</a>
 

 

