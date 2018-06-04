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

# _CERT_LOGOTYPE_EXT_INFO structure


## -description


The <b>CERT_LOGOTYPE_EXT_INFO</b> structure contains a set of logotype information.


## -struct-fields




### -field cCommunityLogo

The number of elements in the <b>rgCommunityLogo</b> array.


### -field rgCommunityLogo

An array of <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structures that contain the community logotypes. The <b>cCommunityLogo</b>  member contains the number of elements in this array.


### -field pIssuerLogo

The address of a <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structure that contains the issuer logotype. This member is optional and may be <b>NULL</b>.


### -field pSubjectLogo

The address of a <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structure that contains the subject logotype. This member is optional and may be <b>NULL</b>.


### -field cOtherLogo

The number of elements in the <b>rgOtherLogo</b> array.


### -field rgOtherLogo

An array of <a href="https://msdn.microsoft.com/104cc412-a268-4b5f-bb9d-9df27f4df6b7">CERT_OTHER_LOGOTYPE_INFO</a> structures that contain any other logotypes. The <b>cOtherLogo</b>  member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>
 

 

