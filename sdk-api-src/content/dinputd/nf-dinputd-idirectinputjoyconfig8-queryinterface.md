---
UID: NF:dinputd.IDirectInputJoyConfig8.QueryInterface
title: IDirectInputJoyConfig8::QueryInterface
author: windows-sdk-content
description: The IDirectInputJoyConfig8::QueryInterface method determines whether the DirectInputJoyConfig object supports a particular COM interface.
old-location: hid\idirectinputjoyconfig8_queryinterface.htm
old-project: hid
ms.assetid: aadd7919-2cb1-4c1e-944d-2ccca2f72b3f
ms.author: windowssdkdev
ms.date: 04/30/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],QueryInterface method, IDirectInputJoyConfig8.QueryInterface, IDirectInputJoyConfig8::QueryInterface, QueryInterface, QueryInterface method [Human Input Devices], QueryInterface method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_757b488f-c54a-4661-9406-d7eb2cbd9dd7.xml, dinputd/IDirectInputJoyConfig8::QueryInterface, hid.idirectinputjoyconfig8_queryinterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
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
tech.root: 
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dinputd.h
api_name:
-	IDirectInputJoyConfig8.QueryInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputJoyConfig8::QueryInterface


## -description


The <b>IDirectInputJoyConfig8::QueryInterface </b>method determines whether the DirectInputJoyConfig object supports a particular COM interface. If it does, the system increases the reference count for the object by 1, and the application can begin using that interface immediately. This method is part of the <b>IUnknown</b> interface inherited by DirectInputJoyConfig. 


## -parameters




### -param riid

Reference identifier of the interface being requested. 


### -param ppvObj

Address of a pointer to be filled with the interface pointer if the query is successful. 


## -returns



Returns DI_OK if successful; otherwise, returns E_NOINTERFACE. 




## -remarks



When the application no longer needs to use the interface obtained by calling this method, it must call the <b>Release</b> method for that interface to free it. 



