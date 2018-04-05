---
UID: NF:appxpackaging.IAppxBlockMapFilesEnumerator.GetCurrent
title: IAppxBlockMapFilesEnumerator::GetCurrent method
author: windows-driver-content
description: Gets the file at the current position of the enumerator.
old-location: appxpkg\iappxblockmapfilesenumerator_getcurrent.htm
old-project: appxpkg
ms.assetid: 6911EBF6-6D0A-4BA5-AD88-3F173141FA5B
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetCurrent method [App packaging and management], GetCurrent method [App packaging and management], IAppxBlockMapFilesEnumerator interface, GetCurrent,IAppxBlockMapFilesEnumerator.GetCurrent, IAppxBlockMapFilesEnumerator, IAppxBlockMapFilesEnumerator interface [App packaging and management], GetCurrent method, IAppxBlockMapFilesEnumerator::GetCurrent, appxpackaging/IAppxBlockMapFilesEnumerator::GetCurrent, appxpkg.iappxblockmapfilesenumerator_getcurrent
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBlockMapFilesEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapFilesEnumerator::GetCurrent method


## -description


Gets the file at the current position of the enumerator.


## -parameters




### -param file [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4C380E2F-8125-4147-97F5-BEDF5BEFB81D">IAppxBlockMapFile</a>**</b>

The current file.


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



The enumerator returned can be empty. In this case, a call to  <a href="https://msdn.microsoft.com/B0021CBC-9A3F-4D2D-8898-FE797396B312">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="https://msdn.microsoft.com/C50F7801-4C33-46EA-989C-259BA407C96B">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.




## -see-also




<a href="https://msdn.microsoft.com/AC2E55C3-1EEF-4867-BECC-37F6269029D6">IAppxBlockMapFilesEnumerator</a>
 

 

