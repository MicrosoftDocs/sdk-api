---
UID: NF:mspcall.CMSPCallBase.MSPCallRelease
title: CMSPCallBase::MSPCallRelease (mspcall.h)
description: The MSPCallRelease method is the private Release method for the call object.
helpviewer_keywords: ["CMSPCallBase interface [TAPI 2.2]","MSPCallRelease method","CMSPCallBase.MSPCallRelease","CMSPCallBase::MSPCallRelease","MSPCallRelease","MSPCallRelease method [TAPI 2.2]","MSPCallRelease method [TAPI 2.2]","CMSPCallBase interface","_tapi3_cmspcallbase_mspcallrelease","mspcall/CMSPCallBase::MSPCallRelease","tapi3.cmspcallbase_mspcallrelease"]
old-location: tapi3\cmspcallbase_mspcallrelease.htm
tech.root: tapi3
ms.assetid: 662361f2-ce0c-4c07-88c1-30393a236bf6
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],MSPCallRelease method, CMSPCallBase.MSPCallRelease, CMSPCallBase::MSPCallRelease, MSPCallRelease, MSPCallRelease method [TAPI 2.2], MSPCallRelease method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_mspcallrelease, mspcall/CMSPCallBase::MSPCallRelease, tapi3.cmspcallbase_mspcallrelease
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPCallBase::MSPCallRelease
 - mspcall/CMSPCallBase::MSPCallRelease
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.MSPCallRelease
---

# CMSPCallBase::MSPCallRelease


## -description

The 
<b>MSPCallRelease</b> method is the private Release method for the call object. MSP objects that keep references to the call object must call this method instead of the normal COM Release method so that the reference is kept on the MSP call object instead of on the aggregate TAPI call object. This is crucial to ensure correct object lifetimes. A template helper function, <b>MSPReleaseHelper</b>, is provided to help the derived MSP implement this method. All the derived MSP has to do in its implementation of this method is call "MSPReleaseHelper(this)". This is needed simply to provide the type of the derived class to the template helper function.



## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>
