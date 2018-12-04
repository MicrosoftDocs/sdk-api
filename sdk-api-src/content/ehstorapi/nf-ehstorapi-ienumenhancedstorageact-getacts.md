---
UID: NF:ehstorapi.IEnumEnhancedStorageACT.GetACTs
title: IEnumEnhancedStorageACT::GetACTs
author: windows-sdk-content
description: Returns an enumeration of all the Addressable Command Targets (ACT) currently connected to the system. If at least one ACT is present, the Enhanced Storage API allocates an array of 1 or more IEnumEnhancedStorageACT pointers.
old-location: enstor\ienumenhancedstorageact_getacts.htm
tech.root: enstor
ms.assetid: 139bb8ed-faca-4fe7-ab6f-63c71d25a711
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetACTs, GetACTs method [Enhanced Storage], GetACTs method [Enhanced Storage],IEnumEnhancedStorageACT interface, IEnumEnhancedStorageACT interface [Enhanced Storage],GetACTs method, IEnumEnhancedStorageACT.GetACTs, IEnumEnhancedStorageACT::GetACTs, ehstorapi/IEnumEnhancedStorageACT::GetACTs, enstor.ienumenhancedstorageact_getacts
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnumEnhancedStorageACT.GetACTs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumEnhancedStorageACT::GetACTs


## -description


Returns an enumeration of all the Addressable Command Targets (ACT) currently connected to the system. If at least one ACT is present, the Enhanced Storage API allocates an array of 1 or more <a href="https://msdn.microsoft.com/807834cc-0f52-43f6-a3b3-06591ba68c15">IEnumEnhancedStorageACT</a> pointers.


## -parameters




### -param pppIEnhancedStorageACTs [out]

Array of <a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a> interface pointers that represent the ACTs for all devices connected to the system. This array is allocated within the API.


### -param pcEnhancedStorageACTs

Count of <a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a> pointers returned. This is the dimension of the  array represented by <i>pppIEnhancedStorageACTs</i>.


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
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
One or more ACTs were found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
pppIEnhancedStorageACTs or pcEnhancedStorageACTs is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Operation failed due to insufficient memory.

</td>
</tr>
</table>
 




## -remarks



The memory containing the array of <a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a> interfaces is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> method.




## -see-also




<a href="https://msdn.microsoft.com/807834cc-0f52-43f6-a3b3-06591ba68c15">IEnumEnhancedStorageACT</a>
 

 

