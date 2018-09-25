---
UID: NF:certenroll.IX509SCEPEnrollment.ProcessResponseMessage
title: IX509SCEPEnrollment::ProcessResponseMessage
author: windows-sdk-content
description: Process a response message and return the disposition of the message.
old-location: security\ix509scepenrollment_processresponsemessage.htm
tech.root: seccertenroll
ms.assetid: 4254fdf3-473f-4f22-a08f-13481fd9f779
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509SCEPEnrollment interface [Security],ProcessResponseMessage method, IX509SCEPEnrollment.ProcessResponseMessage, IX509SCEPEnrollment::ProcessResponseMessage, ProcessResponseMessage, ProcessResponseMessage method [Security], ProcessResponseMessage method [Security],IX509SCEPEnrollment interface, certenroll/IX509SCEPEnrollment::ProcessResponseMessage, security.ix509scepenrollment_processresponsemessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509SCEPEnrollment.ProcessResponseMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SCEPEnrollment::ProcessResponseMessage


## -description


Process a response message and return the disposition of the message.


## -parameters




### -param strResponse [in]


### -param Encoding [in]


### -param pDisposition [out, retval]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You must call the <a href="https://msdn.microsoft.com/en-us/library/Dn424981(v=VS.85).aspx">Initialize</a> and <a href="https://msdn.microsoft.com/en-us/library/Dn424976(v=VS.85).aspx">CreateRequestMessage</a> methods or the <a href="https://msdn.microsoft.com/en-us/library/Dn424982(v=VS.85).aspx">InitializeForPending</a> method before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn424973(v=VS.85).aspx">IX509SCEPEnrollment</a>
 

 

