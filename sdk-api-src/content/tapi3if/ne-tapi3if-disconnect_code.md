---
UID: NE:tapi3if.DISCONNECT_CODE
title: DISCONNECT_CODE (tapi3if.h)
author: windows-sdk-content
description: The DISCONNECT_CODE enum is used by the ITBasicCallControl::Disconnect method.
old-location: tapi3\disconnect_code.htm
tech.root: Tapi
ms.assetid: 90e7b63f-3e19-422d-b45b-43408de9c6cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DC_NOANSWER, DC_NORMAL, DC_REJECTED, DISCONNECT_CODE, DISCONNECT_CODE enumeration [TAPI 2.2], _tapi3_disconnect_code, tapi3.disconnect_code, tapi3if/DC_NOANSWER, tapi3if/DC_NORMAL, tapi3if/DC_REJECTED, tapi3if/DISCONNECT_CODE
ms.topic: enum
f1_keywords: 
 - "tapi3if/DISCONNECT_CODE"
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
 - DISCONNECT_CODE
targetos: Windows
req.typenames: DISCONNECT_CODE
req.redist: 
ms.custom: 19H1
---

# DISCONNECT_CODE enumeration


## -description


The 
<b>DISCONNECT_CODE</b> enum is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">ITBasicCallControl::Disconnect</a> method.


## -enum-fields




### -field DC_NORMAL

The call is being disconnected as part of the normal cycle of the call.


### -field DC_NOANSWER

The call is being disconnected because it has not been answered. (For example, an application may set a certain amount of time for the user to answer the call. If the user does not answer, the application can call 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">Disconnect</a> with the NOANSWER code.)


### -field DC_REJECTED

The user rejected the offered call.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">ITBasicCallControl::Disconnect</a>
 

 

