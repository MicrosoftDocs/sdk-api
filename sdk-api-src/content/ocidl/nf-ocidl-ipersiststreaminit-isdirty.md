---
UID: NF:ocidl.IPersistStreamInit.IsDirty
title: IPersistStreamInit::IsDirty
author: windows-sdk-content
description: Determines whether an object has changed since it was last saved to its stream.
old-location: com\ipersiststreaminit_isdirty.htm
old-project: com
ms.assetid: 2b84818d-0d9d-4f55-8031-b4336baa6c09
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IPersistStreamInit interface [COM],IsDirty method, IPersistStreamInit.IsDirty, IPersistStreamInit::IsDirty, IsDirty, IsDirty method [COM], IsDirty method [COM],IPersistStreamInit interface, _com_ipersiststreaminit_isdirty, com.ipersiststreaminit_isdirty, ocidl/IPersistStreamInit::IsDirty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPersistStreamInit.IsDirty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPersistStreamInit::IsDirty


## -description


Determines whether an object has changed since it was last saved to its stream.


## -parameters






## -returns



This method returns S_OK to indicate that the object has changed. Otherwise, it returns S_FALSE.




## -remarks



Use this method to determine whether an object should be saved before closing it. The dirty flag for an object is conditionally cleared in the <a href="https://msdn.microsoft.com/f88b61d0-dd85-4e8e-b445-dfced6521981">IPersistStreamInit::Save</a> method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You should treat any error return codes as an indication that the object has changed. Unless this method explicitly returns S_FALSE, assume that the object must be saved.

Note that the OLE-provided implementations of the <b>IPersistStreamInit::IsDirty</b> method in the OLE-provided moniker interfaces always return S_FALSE because their internal state never changes.




## -see-also




<a href="https://msdn.microsoft.com/49c413b3-3523-4602-9ec1-19f4e0fe5651">IPersistStreamInit</a>
 

 

