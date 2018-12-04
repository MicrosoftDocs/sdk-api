---
UID: NF:objsel.IDsObjectPicker.Initialize
title: IDsObjectPicker::Initialize
author: windows-sdk-content
description: The IDsObjectPicker::Initialize method initializes the object picker dialog box with data about the scopes, filters, and options used by the object picker dialog box.
old-location: ad\idsobjectpicker_initialize.htm
tech.root: ad
ms.assetid: bcf4d283-6709-4425-a122-8f0808502b58
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IDsObjectPicker interface [Active Directory],Initialize method, IDsObjectPicker.Initialize, IDsObjectPicker::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsObjectPicker interface, _glines_idsobjectpicker_initialize, ad.idsobjectpicker__initialize, ad.idsobjectpicker_initialize, objsel/IDsObjectPicker::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Objsel.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Objsel.dll
api_name:
 - IDsObjectPicker.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsObjectPicker::Initialize


## -description


The <b>IDsObjectPicker::Initialize</b> method initializes the object picker dialog box with data about the scopes, filters, and options used by the object picker dialog box.


## -parameters




### -param pInitInfo

Pointer to a 
<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a> structure that contains the initialization data.


## -returns



Returns a standard error code or one of the following values.




## -remarks



<b>IDsObjectPicker::Initialize</b> can be called more than once and the last call takes precedence. The <a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a> object will completely re-initialize itself in response  to this method.




## -see-also




<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/f2f9da7d-7a09-4b49-a750-078a4573e213">IDsObjectPicker</a>
 

 

