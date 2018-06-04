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

# _CRL_ISSUING_DIST_POINT structure


## -description


The <b>CRL_ISSUING_DIST_POINT</b> structure contains information about the kinds of certificates listed in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).


## -struct-fields




### -field DistPointName

Optional 
<a href="https://msdn.microsoft.com/f47283c3-34f5-4611-b041-456d28d85dbe">CRL_DIST_POINT_NAME</a> member.


### -field fOnlyContainsUserCerts

<b>BOOL</b> flag. <b>TRUE</b> if only user certificates are contained in the CRL.


### -field fOnlyContainsCACerts

<b>BOOL</b> flag. <b>TRUE</b> if only CA certificates are contained in the CRL.


### -field OnlySomeReasonFlags

Optional 
<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a> with bits indicating some reasons for certificate revocation.


### -field fIndirectCRL

<b>BOOL</b> flag. <b>TRUE</b> if this is an indirect CRL.

