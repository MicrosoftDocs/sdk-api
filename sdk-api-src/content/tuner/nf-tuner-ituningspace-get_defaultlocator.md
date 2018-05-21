---
UID: NF:tuner.ITuningSpace.get_DefaultLocator
title: ITuningSpace::get_DefaultLocator
author: windows-driver-content
description: The get_DefaultLocator method retrieves the default locator for this tuning space.
old-location: mstv\ituningspace_get_defaultlocator.htm
old-project: mstv
ms.assetid: facc14bd-182e-4b8e-a567-1bf1d3c4ff36
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_DefaultLocator method, ITuningSpace.get_DefaultLocator, ITuningSpace::get_DefaultLocator, ITuningSpaceget_DefaultLocator, get_DefaultLocator, get_DefaultLocator method [Microsoft TV Technologies], get_DefaultLocator method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_defaultlocator, tuner/ITuningSpace::get_DefaultLocator
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpace.get_DefaultLocator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get_DefaultLocator


## -description



The <b>get_DefaultLocator</b> method retrieves the default locator for this tuning space.




## -parameters




### -param LocatorVal






#### - ppLocatorVal [out]

Address of a variable that receives a pointer to <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The tuning space might not have a default locator. It is the application's responsibility to provide a default locator for the tuning space if needed.

If the tuning space does not have a default locator, this method succeeds but returns the value <b>NULL</b> in the <i>ppLocatorVal</i> parameter. Check for a <b>NULL</b> value before attempting to dereference the pointer.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>



<a href="https://msdn.microsoft.com/59065cc9-8a11-4551-ad3d-e7963628aa20">ITuningSpace::put_DefaultLocator</a>
 

 

