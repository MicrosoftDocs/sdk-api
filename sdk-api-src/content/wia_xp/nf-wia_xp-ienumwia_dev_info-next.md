---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IEnumWIA_DEV_INFO::Next


## -description


The <b>IEnumWIA_DEV_INFO::Next</b> method fills an array of pointers to <a href="https://msdn.microsoft.com/b80d22d4-8e36-484a-9dd1-f228e2236eaf">IWiaPropertyStorage</a> interfaces.



## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of array elements in the array indicated by the <i>rgelt</i> parameter.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/b80d22d4-8e36-484a-9dd1-f228e2236eaf">IWiaPropertyStorage</a>**</b>

Receives the address of an array of <a href="https://msdn.microsoft.com/b80d22d4-8e36-484a-9dd1-f228e2236eaf">IWiaPropertyStorage</a> interface pointers. <b>IEnumWIA_DEV_INFO::Next</b> fills this array with interface pointers.



### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, this parameter contains the number of interface pointers actually stored in the array indicated by the <i>rgelt</i> parameter.



## -returns



Type: <b>HRESULT</b>

While there are devices left to enumerate, this method returns S_OK. It returns S_FALSE when the enumeration is finished. If the method fails, it returns a standard COM error code.




## -remarks



Applications use this method to query the properties of each available Windows Image Acquisition (WIA) hardware device. To do so, the application passes an array of <a href="https://msdn.microsoft.com/b80d22d4-8e36-484a-9dd1-f228e2236eaf">IWiaPropertyStorage</a> interface pointers that it allocates. It also passes the number of array elements in the parameter <i>celt</i>. The <b>IEnumWIA_DEV_INFO::Next</b> method fills the array with pointers to <b>IWiaPropertyStorage</b> interfaces. Applications can query the interfaces for the properties that the device supports.

Applications must call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>rgelt</i> parameter.



