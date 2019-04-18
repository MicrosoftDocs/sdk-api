---
UID: NE:ctfutb.__MIDL_ITfLangBarItemBalloon_0001
title: TfLBBalloonStyle (ctfutb.h)
author: windows-sdk-content
description: Elements of the TfLBBalloonStyle enumeration are used to specify a language bar balloon style.
old-location: tsf\tflbballoonstyle.htm
tech.root: TSF
ms.assetid: c79eb490-b950-4d49-bdf9-821f3706446d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TF_LB_BALLOON_MISS, TF_LB_BALLOON_RECO, TF_LB_BALLOON_SHOW, TfLBBalloonStyle, TfLBBalloonStyle enumeration [Text Services Framework], _tsf_tflbballoonstyle_ref, ctfutb/TF_LB_BALLOON_MISS, ctfutb/TF_LB_BALLOON_RECO, ctfutb/TF_LB_BALLOON_SHOW, ctfutb/TfLBBalloonStyle, tsf.tflbballoonstyle
ms.topic: enum
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ctfutb.h
api_name:
 - TfLBBalloonStyle
product: Windows
targetos: Windows
req.typenames: TfLBBalloonStyle
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# TfLBBalloonStyle enumeration


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




<a href="https://msdn.microsoft.com/b395d587-02a7-496e-8bfd-8fcaba2a3edc">ITfFnBalloon::UpdateBalloon
      </a>



<a href="https://msdn.microsoft.com/8ceed1ae-27f9-4998-b950-52865bfa2f79">TF_LBBALLOONINFO
      </a>
 

 

