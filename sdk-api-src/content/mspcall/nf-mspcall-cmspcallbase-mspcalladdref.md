---
UID: NF:mspcall.CMSPCallBase.MSPCallAddRef
title: CMSPCallBase::MSPCallAddRef (mspcall.h)
description: The MSPCallAddRef method is the private AddRef method for the call object.
helpviewer_keywords: ["CMSPCallBase interface [TAPI 2.2]","MSPCallAddRef method","CMSPCallBase.MSPCallAddRef","CMSPCallBase::MSPCallAddRef","MSPCallAddRef","MSPCallAddRef method [TAPI 2.2]","MSPCallAddRef method [TAPI 2.2]","CMSPCallBase interface","_tapi3_cmspcallbase_mspcalladdref","mspcall/CMSPCallBase::MSPCallAddRef","tapi3.cmspcallbase_mspcalladdref"]
old-location: tapi3\cmspcallbase_mspcalladdref.htm
tech.root: tapi3
ms.assetid: fe70ceac-660e-4fdd-960f-b61503bc8939
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],MSPCallAddRef method, CMSPCallBase.MSPCallAddRef, CMSPCallBase::MSPCallAddRef, MSPCallAddRef, MSPCallAddRef method [TAPI 2.2], MSPCallAddRef method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_mspcalladdref, mspcall/CMSPCallBase::MSPCallAddRef, tapi3.cmspcallbase_mspcalladdref
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
 - CMSPCallBase::MSPCallAddRef
 - mspcall/CMSPCallBase::MSPCallAddRef
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
 - CMSPCallBase.MSPCallAddRef
---

# CMSPCallBase::MSPCallAddRef


## -description

The 
<b>MSPCallAddRef</b> method is the private AddRef method for the call object. MSP objects that keep references to the call object must call this method instead of the normal COM AddRef method so that the reference is kept on the MSP call object instead of on the aggregate TAPI call object. This is crucial to ensure correct object lifetimes. A template helper function, <b>MSPAddRefHelper</b>, is provided to help the derived MSP implement this method. All the derived MSP has to do in its implementation of this method is call "MSPAddRefHelper(this)". This is needed simply to provide the type of the derived class to the template helper function.



## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>
