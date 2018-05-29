---
UID: NF:ehstorapi.IEnhancedStorageACT.GetSilos
title: IEnhancedStorageACT::GetSilos
author: windows-sdk-content
description: Returns an enumeration of all silos associated with the Addressable Command Target (ACT).
old-location: enstor\ienhancedstorageact_getsilos.htm
old-project: enstor
ms.assetid: 823da812-b3f5-4c61-bb33-cd970695879f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetSilos, GetSilos method [Enhanced Storage], GetSilos method [Enhanced Storage],IEnhancedStorageACT interface, IEnhancedStorageACT interface [Enhanced Storage],GetSilos method, IEnhancedStorageACT.GetSilos, IEnhancedStorageACT::GetSilos, ehstorapi/IEnhancedStorageACT::GetSilos, enstor.ienhancedstorageact_getsilos
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EhStorAPI.h
api_name:
-	IEnhancedStorageACT.GetSilos
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnhancedStorageACT::GetSilos


## -description


Returns an enumeration of all  silos associated with the Addressable Command Target (ACT).


## -parameters




### -param pppIEnhancedStorageSilos




### -param pcEnhancedStorageSilos [out]

Count of <a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a> pointers returned. This value indicates the dimension of the  array represented by <i>pppIEnhancedStorageSilos</i>.


#### - ppIEnhancedStorageSilos [out]

Returns an array of one or more <a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a> interface pointers associated with  the ACT.


## -returns



This method can return one of these values.

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
Command was sent successfully and all associated silos have been enumerated. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Command failed due to insufficient memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pppIEnhancedStorageSilos</i> or <i>pcEnhancedStorageSilos</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The memory containing the array of <a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a> interfaces is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a>



<a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a>
 

 

