---
UID: NE:tapi3if.PHONE_PRIVILEGE
title: PHONE_PRIVILEGE
author: windows-sdk-content
description: The PHONE_PRIVILEGE enum indicates the application's privilege status with respect to the current phone device.
old-location: tapi3\phone_privilege.htm
tech.root: tapi
ms.assetid: f1c162c6-058d-4cf2-a493-17b7752ffeeb
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PHONE_PRIVILEGE, PHONE_PRIVILEGE enumeration [TAPI 2.2], PP_MONITOR, PP_OWNER, _tapi3_phone_privilege, tapi3.phone_privilege, tapi3if/PHONE_PRIVILEGE, tapi3if/PP_MONITOR, tapi3if/PP_OWNER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - PHONE_PRIVILEGE
product: Windows
targetos: Windows
req.typenames: PHONE_PRIVILEGE
req.redist: 
---

# PHONE_PRIVILEGE enumeration


## -description


The 
<b>PHONE_PRIVILEGE</b> enum indicates the application's privilege status with respect to the current phone device.


## -enum-fields




### -field PP_OWNER

The application has owner privileges for the current phone session.


### -field PP_MONITOR

The application has monitor privileges for the current phone session.


## -see-also




<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a>



<a href="https://msdn.microsoft.com/88103a48-a5cd-43a7-a88e-9b16313b35c2">ITPhone::get_Privilege</a>
 

 

