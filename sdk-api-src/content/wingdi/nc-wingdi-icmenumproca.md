---
UID: NC:wingdi.ICMENUMPROCA
title: ICMENUMPROCA (wingdi.h)

description: The EnumICMProfilesProcCallback callback is an application-defined callback function that processes color profile data from EnumICMProfiles .
old-location: wcs\enumicmprofilesproccallback.htm
tech.root: WCS
ms.assetid: 6e8f4ce5-c546-4e6a-8f35-4a22d60b6754

ms.date: 12/05/2018
ms.keywords: ICMENUMPROC, ICMENUMPROC callback, ICMENUMPROC callback function [Windows Color System], ICMENUMPROCA, ICMENUMPROCW, _color_EnumICMProfilesProcCallback, wcs.enumicmprofilesproccallback, wingdi/ICMENUMPROC, wingdi/ICMENUMPROCA, wingdi/ICMENUMPROCW
ms.topic: callback
f1_keywords: 
 - "wingdi/ICMENUMPROC"
dev_langs:
 - c++
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ICMENUMPROCW (Unicode) and ICMENUMPROCA (ANSI)
req.idl: 
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
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - ICMENUMPROC
 - ICMENUMPROCA
 - ICMENUMPROCW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICMENUMPROCA callback function


## -description


The <b>EnumICMProfilesProcCallback</b> callback is an application-defined callback function that processes color profile data from <b>EnumICMProfiles</b> .


## -parameters




### -param Arg1


### -param Arg2








#### - lParam

Data supplied by the application that is passed to the callback function by the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumicmprofilesa">EnumICMProfiles</a> function.


#### - lpszFilename

Pointer to the file name of the color profile.


## -returns



This function must return a positive value to continue enumeration, or zero to stop enumeration. It may not return a negative value.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-enumicmprofilesa">EnumICMProfiles</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>
 

 

