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

# IAccessibleWindowlessSite::ReleaseObjectIdRange


## -description


Releases an object ID range that was acquired by a previous call to the <a href="https://msdn.microsoft.com/EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4">IAccessibleWindowlessSite::AcquireObjectIdRange</a> method.


## -parameters




### -param rangeBase [in]

Type: <b>long</b>

The first object ID in the range of IDs to be released.


### -param pRangeOwner [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1b6b2c02-f3b5-4a8a-9388-b3833cd0cd44">IAccessibleHandler</a>*</b>

The windowless ActiveX control with which the range was associated when it was acquired.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To prevent mistakes when releasing object ranges, the system uses the <i>pControl</i> parameter to ensure that the range of object IDs being released actually belongs to the specified windowless control.  




## -see-also




<a href="https://msdn.microsoft.com/1ED23B39-231B-46A2-9FED-969A36DA8DD9">IAccessibleWindowlessSite</a>



<a href="https://msdn.microsoft.com/EB8BAD4D-0C8F-4926-A1B4-383D03C3B0C4">IAccessibleWindowlessSite::AcquireObjectIdRange</a>
 

 

