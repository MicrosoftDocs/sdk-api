---
UID: NC:projectedfslib.PRJ_GET_PLACEHOLDER_INFO_CB
title: PRJ_GET_PLACEHOLDER_INFO_CB
author: windows-sdk-content
description: Requests information for a file or directory from the provider.
old-location: projfs\prj_get_placeholder_info_cb.htm
tech.root: ProjFS
ms.assetid: 1BC7C1FA-1BAB-48FB-85C2-34EC3B1B4167
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: PRJ_GET_PLACEHOLDER_INFO_CB, PRJ_GET_PLACEHOLDER_INFO_CB callback, PRJ_GET_PLACEHOLDER_INFO_CB callback function, ProjFS.prj_get_placeholder_info_cb, projectedfslib/PRJ_GET_PLACEHOLDER_INFO_CB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_GET_PLACEHOLDER_INFO_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_GET_PLACEHOLDER_INFO_CB callback function


## -description


Requests information for a file or directory from the provider.


## -parameters




### -param callbackData [in]

Information about the operation. The following <i>callbackData</i> members are necessary to implement this callback:<dl>
<dd><b>FilePathName</b>Identifies the path to the file or directory in the provider's store for which ProjFS is requesting information.

The provider uses this to determine whether the name exists in its backing store.  It should use the <a href="projfs.prjfilenamematch">PrjFileNameMatch</a> function to compare this name to the names in its store.  If it finds a matching name, it uses that name as the <i>destinationFileName</i> parameter of the <a href="projfs.prjwriteplaceholderinfo">PrjWritePlaceholderInfo</a> function.

</dd>
<dd><b>VersionInfo</b>Provides version information for the parent directory of the requested item.

</dd>
</dl>


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it. 


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The file exists in the provider's store and it successfully gave the file's information to ProjFS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_IO_PENDING)</b></dt>
</dl>
</td>
<td width="60%">
The provider wishes to complete the operation at a later time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The file does not exist in the provider's store. 


</td>
</tr>
</table>
 

Another appropriate HRESULT error code if the provider fails the operation. 




## -remarks



ProjFS will use the information provided in this callback to create a placeholder for the requested item. 


To handle this callback, the provider calls <a href="projfs.prjwriteplaceholderinfo">PrjWritePlaceholderInfo</a> to give ProjFS the information for the requested file name. Then the provider completes the callback.



