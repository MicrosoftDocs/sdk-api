---
UID: NF:mspcall.CMSPCallBase.MSPCallRelease
title: CMSPCallBase::MSPCallRelease
author: windows-sdk-content
description: The MSPCallRelease method is the private Release method for the call object.
old-location: tapi3\cmspcallbase_mspcallrelease.htm
old-project: tapi
ms.assetid: 662361f2-ce0c-4c07-88c1-30393a236bf6
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],MSPCallRelease method, CMSPCallBase.MSPCallRelease, CMSPCallBase::MSPCallRelease, MSPCallRelease, MSPCallRelease method [TAPI 2.2], MSPCallRelease method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_mspcallrelease, mspcall/CMSPCallBase::MSPCallRelease, tapi3.cmspcallbase_mspcallrelease
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mspcall.h
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.MSPCallRelease
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallBase::MSPCallRelease


## -description


The 
<b>MSPCallRelease</b> method is the private Release method for the call object. MSP objects that keep references to the call object must call this method instead of the normal COM Release method so that the reference is kept on the MSP call object instead of on the aggregate TAPI call object. This is crucial to ensure correct object lifetimes. A template helper function, <b>MSPReleaseHelper</b>, is provided to help the derived MSP implement this method. All the derived MSP has to do in its implementation of this method is call "MSPReleaseHelper(this)". This is needed simply to provide the type of the derived class to the template helper function.


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

