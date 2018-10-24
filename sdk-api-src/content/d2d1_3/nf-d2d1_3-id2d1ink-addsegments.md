---
UID: NF:d2d1_3.ID2D1Ink.AddSegments
title: ID2D1Ink::AddSegments
author: windows-sdk-content
description: Adds the given segments to the end of this ink object.
old-location: direct2d\id2d1ink_addsegments.htm
tech.root: Direct2D
ms.assetid: 0AB546AC-F7AB-4C48-AA10-3DD2FF11B853
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AddSegments, AddSegments method [Direct2D], AddSegments method [Direct2D],ID2D1Ink interface, ID2D1Ink interface [Direct2D],AddSegments method, ID2D1Ink.AddSegments, ID2D1Ink::AddSegments, d2d1_3/ID2D1Ink::AddSegments, direct2d.id2d1ink_addsegments
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Ink.AddSegments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Ink::AddSegments


## -description


Adds the given segments to the end of this ink object.


## -parameters




### -param segments [in]

Type: <b>const <a href="https://msdn.microsoft.com/27F1F78B-2478-4F5D-BF56-9931E767C358">D2D1_INK_BEZIER_SEGMENT</a>*</b>

A pointer to an array of segments to be added to this ink object.


### -param segmentsCount

Type: <b>UINT32</b>

The number of segments to be added to this ink object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a>
 

 

