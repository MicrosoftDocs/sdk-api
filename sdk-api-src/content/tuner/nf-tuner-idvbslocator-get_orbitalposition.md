---
UID: NF:tuner.IDVBSLocator.get_OrbitalPosition
title: IDVBSLocator::get_OrbitalPosition
author: windows-sdk-content
description: The get_OrbitalPosition method retrieves the setting for the satellite's orbital position.
old-location: mstv\idvbslocator_get_orbitalposition.htm
old-project: mstv
ms.assetid: 3069cf27-32db-4d3f-9e61-9eddc266b540
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_OrbitalPosition method, IDVBSLocator.get_OrbitalPosition, IDVBSLocator::get_OrbitalPosition, IDVBSLocatorget_OrbitalPosition, get_OrbitalPosition, get_OrbitalPosition method [Microsoft TV Technologies], get_OrbitalPosition method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_orbitalposition, tuner/IDVBSLocator::get_OrbitalPosition
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IDVBSLocator.get_OrbitalPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSLocator::get_OrbitalPosition


## -description



The <b>get_OrbitalPosition</b> method retrieves the setting for the satellite's orbital position.




## -parameters




### -param longitude






#### - plongitude [out]

Receives the longitude setting in tenths of a degree.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/a9f02e78-3800-4b14-81df-acab01ea072b">IDVBSLocator Interface</a>
 

 

