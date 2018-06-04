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

# __MIDL_ITfLangBarItemBalloon_0001 enumeration


## -description


Elements of the <b>TfLBBalloonStyle</b> enumeration are used to specify a language bar balloon style.


## -enum-fields




### -field TF_LB_BALLOON_RECO

This balloon style is used to represent a reconversion operation.


### -field TF_LB_BALLOON_SHOW

This is a normal balloon style.


### -field TF_LB_BALLOON_MISS

This balloon style is used to indicate that a command was not recognized.


## -remarks



The following image shows an example of a balloon with the TF_LB_BALLOON_RECO style. 

<img alt="TF_LB_BALLOON_RECO balloon" border="border" src="images/Balloon_RECO.gif"/>
The following image shows an example of a balloon with the TF_LB_BALLOON_SHOW style. 

<img alt="TF_LB_BALLOON_SHOW balloon" border="border" src="images/Balloon_SHOW.gif"/>
The following image shows an example of a balloon with the TF_LB_BALLOON_MISS style. 

<img alt="TF_LB_BALLOON_MISS balloon" border="border" src="images/Balloon_MISS.gif"/>



## -see-also




<a href="https://msdn.microsoft.com/b395d587-02a7-496e-8bfd-8fcaba2a3edc">
        ITfFnBalloon::UpdateBalloon
      </a>



<a href="https://msdn.microsoft.com/8ceed1ae-27f9-4998-b950-52865bfa2f79">TF_LBBALLOONINFO
      </a>
 

 

