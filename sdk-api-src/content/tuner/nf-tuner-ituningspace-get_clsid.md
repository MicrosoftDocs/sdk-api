---
UID: NF:tuner.ITuningSpace.get_CLSID
title: ITuningSpace::get_CLSID
author: windows-sdk-content
description: The get_CLSID method gets the CLSID of the tuning space as a BSTR.
old-location: mstv\ituningspace_get_clsid.htm
old-project: mstv
ms.assetid: def4aac2-3d0b-4ce6-9f6b-d13e7c3cc86d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_CLSID method, ITuningSpace.get_CLSID, ITuningSpace::get_CLSID, ITuningSpaceget_CLSID, get_CLSID, get_CLSID method [Microsoft TV Technologies], get_CLSID method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_clsid, tuner/ITuningSpace::get_CLSID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpace.get_CLSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get_CLSID


## -description



The <b>get_CLSID</b> method gets the CLSID of the tuning space as a <b>BSTR</b>.




## -parameters




### -param SpaceCLSID






#### - pSpaceCLSID [out]

Pointer to a variable that receives a string representation of the tuning space CLSID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method provides script access to the <b>IPersist::GetClassID</b> method.

The returned CLSID represents the COM object that implements this tuning space. The CLSID is not guaranteed to be unique to this tuning space, however, because the same object may implement several tuning spaces.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

