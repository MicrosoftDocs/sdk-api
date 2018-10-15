---
UID: NS:wingdi.tagEMRSETICMPROFILE
title: tagEMRSETICMPROFILE
author: windows-sdk-content
description: The EMRSETICMPROFILE structure contains members for the SetICMProfile enhanced metafile record.
old-location: gdi\emrseticmprofile.htm
tech.root: gdi
ms.assetid: 2f43db1e-95eb-4812-9422-ddc9df634c15
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PEMRSETICMPROFILE, *PEMRSETICMPROFILEA, *PEMRSETICMPROFILEW, EMRSETICMPROFILE, EMRSETICMPROFILE structure [Windows GDI], EMRSETICMPROFILEA, EMRSETICMPROFILEA structure [Windows GDI], EMRSETICMPROFILEW, EMRSETICMPROFILEW structure [Windows GDI], PEMRSETICMPROFILE, PEMRSETICMPROFILE structure pointer [Windows GDI], PEMRSETICMPROFILEA, PEMRSETICMPROFILEA structure pointer [Windows GDI], PEMRSETICMPROFILEW, PEMRSETICMPROFILEW structure pointer [Windows GDI], _win32_EMRSETICMPROFILE_str, gdi.emrseticmprofile, tagEMRSETICMPROFILE, wingdi/EMRSETICMPROFILE, wingdi/EMRSETICMPROFILEA, wingdi/EMRSETICMPROFILEW, wingdi/PEMRSETICMPROFILE, wingdi/PEMRSETICMPROFILEA, wingdi/PEMRSETICMPROFILEW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRSETICMPROFILE
product: Windows
targetos: Windows
req.typenames: EMRSETICMPROFILE, *PEMRSETICMPROFILE, EMRSETICMPROFILEA, *PEMRSETICMPROFILEA, EMRSETICMPROFILEW, *PEMRSETICMPROFILEW
req.redist: 
---

# tagEMRSETICMPROFILE structure


## -description



The <b>EMRSETICMPROFILE</b> structure contains members for the <a href="https://msdn.microsoft.com/c95f6536-9377-4766-9eb6-004a41bcf6c5">SetICMProfile</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field dwFlags

The profile flags. This member can be SETICMPROFILE_EMBEDED (0x00000001).


### -field cbName

The size of the desired profile name.


### -field cbData

The size of profile data, if attached.


### -field Data

An array that contains the profile data. The length of this array is <b>cbName</b> plus <b>cbData</b>.


## -remarks



This structure is to be used during metafile playback.




## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/c95f6536-9377-4766-9eb6-004a41bcf6c5">SetICMProfile</a>
 

 

