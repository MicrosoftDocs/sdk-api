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

# _SID_INFO structure


## -description


The <b>SID_INFO</b> structure contains the list of common names corresponding to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structures returned by 
<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>. It is a member of the 
<a href="https://msdn.microsoft.com/e9be644c-ec56-4a49-9aa8-6b3f62d6cf0d">SID_INFO_LIST</a> structure.


## -struct-fields




### -field pSid

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that identifies one of the SIDs passed into 
<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>.


### -field pwzCommonName

A pointer to a string containing the common name corresponding to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified in <b>pSid</b>.


### -field pwzClass

A pointer to a string describing the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure as either a user or a group. The possible values of this string are as follows:

<p class="indent">"Computer"

<p class="indent">"Group"

<p class="indent">"User"


### -field pwzUPN

A pointer to the user principal name (UPN) corresponding to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure specified in <b>pSid</b>. If a UPN has not been designated for the <b>SID</b> structure, the value of this parameter is <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/9a4056c6-6a21-4051-b4a6-c77351fce983">ISecurityInformation2::LookupSids</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

