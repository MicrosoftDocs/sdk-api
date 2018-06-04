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

# _DD_MORESURFACECAPS structure


## -description



   The DD_MORESURFACECAPS structure defines more driver surface capabilities in addition to those described in <a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>.
  


## -struct-fields




### -field dwSize

Specifies the size of this DD_MORESURFACECAPS structure. The DD_MORESURFACECAPS structure is of variable size. There should be exactly <b>DD_HALINFO.vmiData.dwNumHeaps</b> copies of the <b>ddsExtendedHeapRestrictions</b> structure within the array member of this structure. The total size of a DD_MORESURFACECAPS structure is thus: 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>dwSize = 
   sizeof(DD_MORESURFACECAPS) +
   (DD_HALINFO.vmiData.dwNumHeaps - 1) * sizeof(DDSCAPSEX) * 2</pre>
</td>
</tr>
</table></span></div>
This calculation accounts for the minimum size of the DD_MORESURFACECAPS structure, which includes only one <b>ddsExtendedHeapRestrictions</b> array element. Any additional <b>ddsExtendedHeapRestrictions</b> array elements must be accounted for by adding the sizes of the remaining array elements. That is, by adding the product of the number of remaining <b>ddsExtendedHeapRestrictions</b> structures times the size of each one.


### -field ddsCapsMore

Specifies a DDSCAPSEX structure that provides the extensions to <b>ddcaps.ddsCaps</b> that describe the types of extended surfaces the driver can create. When a DDCAPS structure is returned to the application, it is a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a> structure manufactured from <b>DDCAPS.ddsCaps</b> and <b>DD_MORESURFACECAPS.ddsCapsMore</b>. A DDSCAPSEX structure is the same as a DDSCAPS2 structure without the <b>dwCaps</b> member. 


### -field tagNTExtendedHeapRestrictions

 


### -field tagNTExtendedHeapRestrictions.ddsCapsExAlt

 


### -field ddsExtendedHeapRestrictions

Specifies a structure containing two members. These members are filled in by Microsoft DirectX 6.0-aware drivers (and drivers compliant with later versions of DirectX), to restrict the video memory heaps that are exposed to Microsoft DirectDraw to certain sets of DDSCAPS_<i>Xxx</i> bits. The DirectDraw version is determined by looking at DDVERSIONINFO, which is defined in <i>ddrawi.h</i>. The <b>ddsCapsEx</b> and <b>ddsCapsExAlt</b> members of the DD_MORESURFACECAPS structure are exactly analogous to the <b>ddsCaps</b> and <b>ddsCapsAlt</b> members of the VIDEOMEMORY structures listed in the <b>VIDMEMINFO.pvmList</b> member of <b>DD_HALINFO.vmiData</b>. 



#### ddsCapsEx

Specifies a DDSCAPSEX structure in which the driver returns the capabilities for which this chunk of memory cannot be used.



#### ddsCapsExAlt

Specifies a DDSCAPSEX structure in which the driver returns the capabilities for which this chunk of memory cannot be used for when no other memory is found on the first pass.


## -remarks



This structure contains the caps bits added to the <b>DDCAPS.ddsCaps</b> structure in DirectX 6.0. See the DirectDraw SDK documentation for a description of the DDCAPS structure.

<b>Note for Microsoft Windows 98/Me:</b>  DD_MORESURFACECAPS is the definition for Windows 2000 and later versions. Drivers that run on Windows 98/Me use the name DDMORESURFACECAPS, which is aliased in <i>dx95type.h</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549248">DDCORECAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550292">DDSCAPS2</a>
 

 

