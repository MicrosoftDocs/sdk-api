---
UID: NF:tuner.ITuningSpace.get_FriendlyName
title: ITuningSpace::get_FriendlyName
author: windows-sdk-content
description: The get_FriendlyName method retrieves the localized, user-friendly name of the tuning space.
old-location: mstv\ituningspace_get_friendlyname.htm
old-project: mstv
ms.assetid: d1427aae-49e9-45ce-abd9-902a895e6e44
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_FriendlyName method, ITuningSpace.get_FriendlyName, ITuningSpace::get_FriendlyName, ITuningSpaceget_FriendlyName, get_FriendlyName, get_FriendlyName method [Microsoft TV Technologies], get_FriendlyName method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_friendlyname, tuner/ITuningSpace::get_FriendlyName
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	ITuningSpace.get_FriendlyName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpace::get_FriendlyName


## -description



The <b>get_FriendlyName</b> method retrieves the localized, user-friendly name of the tuning space.




## -parameters




### -param Name






#### - pName [out]

Pointer to a variable receives the user-friendly name.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

