---
UID: NF:tuner.IDVBSLocator.get_Azimuth
title: IDVBSLocator::get_Azimuth
author: windows-sdk-content
description: The get_Azimuth method retrieves the azimuth setting used for positioning the satellite dish.
old-location: mstv\idvbslocator_get_azimuth.htm
old-project: mstv
ms.assetid: 2c1314f4-6291-4440-8010-247f8fa82d0c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDVBSLocator interface [Microsoft TV Technologies],get_Azimuth method, IDVBSLocator.get_Azimuth, IDVBSLocator::get_Azimuth, IDVBSLocatorget_Azimuth, get_Azimuth, get_Azimuth method [Microsoft TV Technologies], get_Azimuth method [Microsoft TV Technologies],IDVBSLocator interface, mstv.idvbslocator_get_azimuth, tuner/IDVBSLocator::get_Azimuth
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
 - IDVBSLocator.get_Azimuth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDVBSLocator::get_Azimuth


## -description



The <b>get_Azimuth</b> method retrieves the azimuth setting used for positioning the satellite dish.




## -parameters




### -param Azimuth






#### - pAzimuth [out]

Receives the azimuth in tenths of a degree.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/a9f02e78-3800-4b14-81df-acab01ea072b">IDVBSLocator Interface</a>
 

 

