---
UID: NF:bdaiface.IBDA_ISDBConditionalAccess.SetIsdbCasRequest
title: IBDA_ISDBConditionalAccess::SetIsdbCasRequest
author: windows-sdk-content
description: Sends a conditional access system (CAS) command for Integrated Services Digital Broadcasting (ISDB).
old-location: mstv\ibda_isdbconditionalaccess_setisdbcasrequest.htm
tech.root: mstv
ms.assetid: c93351f5-1829-4405-b665-00f2e78391e0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_ISDBConditionalAccess interface [Microsoft TV Technologies],SetIsdbCasRequest method, IBDA_ISDBConditionalAccess.SetIsdbCasRequest, IBDA_ISDBConditionalAccess::SetIsdbCasRequest, SetIsdbCasRequest, SetIsdbCasRequest method [Microsoft TV Technologies], SetIsdbCasRequest method [Microsoft TV Technologies],IBDA_ISDBConditionalAccess interface, bdaiface/IBDA_ISDBConditionalAccess::SetIsdbCasRequest, mstv.ibda_isdbconditionalaccess_setisdbcasrequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - bdaiface.h
api_name:
 - IBDA_ISDBConditionalAccess.SetIsdbCasRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_ISDBConditionalAccess.SetIsdbCasRequest
: 
---

# IBDA_ISDBConditionalAccess::SetIsdbCasRequest


## -description


Sends a conditional access system (CAS) command for Integrated Services Digital Broadcasting (ISDB).


## -parameters




### -param ulRequestId [in]

The numeric code for the CAS command. The ARIB standard defines these values. Enumeration constants for some commands are defined in the <a href="https://msdn.microsoft.com/5c8a97bb-9d8b-4f4f-aeab-e8bf199a652e">ISDBCAS_REQUEST_ID</a> enumeration.


### -param ulcbRequestBufferLen [in]

Size of the <i>pbRequestBuffer</i> array, in bytes.


### -param pbRequestBuffer [in]

Pointer to a byte array that contains the data for the command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0e45e5ea-9f38-4a96-be44-8ee123492aa9">IBDA_ISDBConditionalAccess</a>
 

 

