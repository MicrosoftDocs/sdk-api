---
UID: NF:xenroll.ICEnroll4.removePendingRequest
title: ICEnroll4::removePendingRequest
author: windows-sdk-content
description: Removes a pending request from the client's request store. This method was first defined in the ICEnroll4 interface.
old-location: security\icenroll4_removependingrequest.htm
tech.root: seccrypto
ms.assetid: 22ddd7f8-b2c0-4b9a-a2b3-c2cb470d0502
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CEnroll object [Security],removePendingRequest method, ICEnroll4 interface [Security],removePendingRequest method, ICEnroll4.removePendingRequest, ICEnroll4::removePendingRequest, _xen_icenroll4_removependingrequest, removePendingRequest, removePendingRequest method [Security], removePendingRequest method [Security],CEnroll object, removePendingRequest method [Security],ICEnroll4 interface, security.icenroll4_removependingrequest, xenroll/ICEnroll4::removePendingRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.removePendingRequest
 - CEnroll.removePendingRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll4::removePendingRequest


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>removePendingRequest</b> method removes a pending request from the client's request store. This method was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param strThumbprint [in]

The thumbprint, or <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a>, of the certificate data.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



