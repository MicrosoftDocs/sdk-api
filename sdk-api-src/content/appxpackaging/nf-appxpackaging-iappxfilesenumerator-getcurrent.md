---
UID: NF:appxpackaging.IAppxFilesEnumerator.GetCurrent
title: IAppxFilesEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the payload file at the current position of the enumerator.
old-location: appxpkg\iappxfilesenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: AFE7534D-862B-47C5-B6C0-633205E39FAB
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxFilesEnumerator interface, IAppxFilesEnumerator interface [App packaging and management],GetCurrent method, IAppxFilesEnumerator.GetCurrent, IAppxFilesEnumerator::GetCurrent, appxpackaging/IAppxFilesEnumerator::GetCurrent, appxpkg.iappxfilesenumerator_getcurrent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFilesEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFilesEnumerator::GetCurrent


## -description


Gets the payload file at the current position of the enumerator.


## -parameters




### -param file [out, retval]

Type: <b><a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>**</b>

The current payload file.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has passed the last item in the collection.

</td>
</tr>
</table>
 




## -remarks



The enumerator returned can be empty. In this case, a call to  <a href="https://msdn.microsoft.com/4CC798E4-5FD2-45DE-BD3A-0B036601BEDB">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="https://msdn.microsoft.com/EC27AB65-EC67-4F6B-A3B8-313FD0422FA2">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.




## -see-also




<a href="https://msdn.microsoft.com/A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724">IAppxFilesEnumerator</a>
 

 

