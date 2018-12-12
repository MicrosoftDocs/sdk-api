---
UID: NE:mfidl._MFSHUTDOWN_STATUS
title: MFSHUTDOWN_STATUS
author: windows-sdk-content
description: Describes the current status of a call to the IMFShutdown::Shutdown method.
old-location: mf\mfshutdown_status.htm
tech.root: medfound
ms.assetid: a2257260-3f2c-4c6b-88cc-b8927b899782
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFSHUTDOWN_COMPLETED, MFSHUTDOWN_INITIATED, MFSHUTDOWN_STATUS, MFSHUTDOWN_STATUS enumeration [Media Foundation], a2257260-3f2c-4c6b-88cc-b8927b899782, mf.mfshutdown_status, mfidl/MFSHUTDOWN_COMPLETED, mfidl/MFSHUTDOWN_INITIATED, mfidl/MFSHUTDOWN_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFSHUTDOWN_STATUS
product: Windows
targetos: Windows
req.typenames: MFSHUTDOWN_STATUS
req.redist: 
---

# MFSHUTDOWN_STATUS enumeration


## -description


Describes the current status of a call to the <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">IMFShutdown::Shutdown</a> method.


## -enum-fields




### -field MFSHUTDOWN_INITIATED

The shutdown operation has started but is not yet complete.


### -field MFSHUTDOWN_COMPLETED

Shutdown is complete.


## -see-also




<a href="https://msdn.microsoft.com/c3052658-51bb-401b-8db9-3428868899d6">IMFShutdown</a>



<a href="https://msdn.microsoft.com/8cf5f5f3-a3ad-4745-87e8-764ed118477a">IMFShutdown::GetShutdownStatus</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

