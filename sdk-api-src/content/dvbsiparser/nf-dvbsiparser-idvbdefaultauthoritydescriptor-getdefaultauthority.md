---
UID: NF:dvbsiparser.IDvbDefaultAuthorityDescriptor.GetDefaultAuthority
title: IDvbDefaultAuthorityDescriptor::GetDefaultAuthority method
author: windows-driver-content
description: Gets the string identifying the default authority from a Digital Video Broadcast (DVB) content reference identifier (CRID).
old-location: mstv\idvbdefaultauthoritydescriptor_getdefaultauthority.htm
old-project: mstv
ms.assetid: dd615bd1-3db7-4577-aa10-d68ad61b068c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetDefaultAuthority method [Microsoft TV Technologies], GetDefaultAuthority method [Microsoft TV Technologies], IDvbDefaultAuthorityDescriptor interface, GetDefaultAuthority,IDvbDefaultAuthorityDescriptor.GetDefaultAuthority, IDvbDefaultAuthorityDescriptor, IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies], GetDefaultAuthority method, IDvbDefaultAuthorityDescriptor::GetDefaultAuthority, dvbsiparser/IDvbDefaultAuthorityDescriptor::GetDefaultAuthority, mstv.idvbdefaultauthoritydescriptor_getdefaultauthority
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbDefaultAuthorityDescriptor.GetDefaultAuthority
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbDefaultAuthorityDescriptor::GetDefaultAuthority method


## -description


Gets the string identifying the default authority from a Digital Video Broadcast (DVB)
content reference identifier (CRID). 


## -parameters




### -param pbLength [out]

Receives the length of the default authority string in bytes.


### -param ppbBytes [out]

Pointer to a buffer that receives the default authority string. The caller is responsible for releasing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/42d10cb5-dea9-4fdb-a588-7bc647e0b95b">IDvbDefaultAuthorityDescriptor</a>
 

 

