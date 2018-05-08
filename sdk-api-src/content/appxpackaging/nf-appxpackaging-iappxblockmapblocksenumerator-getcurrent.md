---
UID: NF:appxpackaging.IAppxBlockMapBlocksEnumerator.GetCurrent
title: IAppxBlockMapBlocksEnumerator::GetCurrent
author: windows-driver-content
description: Gets the block at the current position of the enumerator.
old-location: appxpkg\iappxblockmapblocksenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: A546BD4D-DA7A-4A50-BD45-2219D70DF0F9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxBlockMapBlocksEnumerator interface, IAppxBlockMapBlocksEnumerator interface [App packaging and management],GetCurrent method, IAppxBlockMapBlocksEnumerator.GetCurrent, IAppxBlockMapBlocksEnumerator::GetCurrent, appxpackaging/IAppxBlockMapBlocksEnumerator::GetCurrent, appxpkg.iappxblockmapblocksenumerator_getcurrent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBlockMapBlocksEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapBlocksEnumerator::GetCurrent


## -description


Gets the block at the current position of the enumerator.


## -parameters




### -param block [out, retval]

Type: <b><a href="https://msdn.microsoft.com/39B0680A-F27B-478F-8E83-FE1BFCF61AC4">IAppxBlockMapBlock</a>**</b>

The current block.


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



The enumerator returned can be empty. In this case, a call to  <a href="https://msdn.microsoft.com/AC12BCDD-201C-4F22-B39E-1349EB84ED00">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="https://msdn.microsoft.com/CDF8C336-CFF8-41FE-AC3E-48988209850E">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.




## -see-also




<a href="https://msdn.microsoft.com/E7678755-4779-4A64-A666-C5FFC4A7F37A">IAppxBlockMapBlocksEnumerator</a>
 

 

