---
UID: NC:wingdi.ICMENUMPROCA
title: ICMENUMPROCA
author: windows-sdk-content
description: The EnumICMProfilesProcCallback callback is an application-defined callback function that processes color profile data from EnumICMProfiles .
old-location: wcs\enumicmprofilesproccallback.htm
old-project: WCS
ms.assetid: 6e8f4ce5-c546-4e6a-8f35-4a22d60b6754
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ICMENUMPROC, ICMENUMPROC callback, ICMENUMPROC callback function [Windows Color System], ICMENUMPROCA, ICMENUMPROCW, _color_EnumICMProfilesProcCallback, wcs.enumicmprofilesproccallback, wingdi/ICMENUMPROC, wingdi/ICMENUMPROCA, wingdi/ICMENUMPROCW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: FAX_TIME, *PFAX_TIME
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ICMENUMPROCA callback function


## -description


The <b>EnumICMProfilesProcCallback</b> callback is an application-defined callback function that processes color profile data from <b>EnumICMProfiles</b> .


## -parameters




### -param Arg1


### -param Arg2








#### - lParam

Data supplied by the application that is passed to the callback function by the <a href="https://msdn.microsoft.com/a93e6239-b6c7-4e37-9f06-03790a3ed53f">EnumICMProfiles</a> function.


#### - lpszFilename

Pointer to the file name of the color profile.


## -returns



This function must return a positive value to continue enumeration, or zero to stop enumeration. It may not return a negative value.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/a93e6239-b6c7-4e37-9f06-03790a3ed53f">EnumICMProfiles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

