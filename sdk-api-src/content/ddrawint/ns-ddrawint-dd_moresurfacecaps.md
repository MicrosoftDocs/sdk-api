---
UID: NS:ddrawint._DD_MORESURFACECAPS
title: DD_MORESURFACECAPS (ddrawint.h)
description: The DD_MORESURFACECAPS structure defines more driver surface capabilities in addition to those described in DDCORECAPS.
helpviewer_keywords: ["*PDD_MORESURFACECAPS","DD_MORESURFACECAPS","DD_MORESURFACECAPS structure [Display Devices]","ddrawint/DD_MORESURFACECAPS","ddstrcts_e28f85ae-f428-4e7c-b142-9892afa24323.xml","display.dd_moresurfacecaps"]
old-location: display\dd_moresurfacecaps.htm
tech.root: display
ms.assetid: 25cc9058-0c37-4768-a177-345cdae4ee5f
ms.date: 12/05/2018
ms.keywords: '*PDD_MORESURFACECAPS, DD_MORESURFACECAPS, DD_MORESURFACECAPS structure [Display Devices], ddrawint/DD_MORESURFACECAPS, ddstrcts_e28f85ae-f428-4e7c-b142-9892afa24323.xml, display.dd_moresurfacecaps'
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: '*PDD_MORESURFACECAPS, DD_MORESURFACECAPS'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_MORESURFACECAPS
 - ddrawint/_DD_MORESURFACECAPS
 - PDD_MORESURFACECAPS
 - ddrawint/PDD_MORESURFACECAPS
 - DD_MORESURFACECAPS
 - ddrawint/DD_MORESURFACECAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_MORESURFACECAPS
---

# DD_MORESURFACECAPS structure


## -description

The DD_MORESURFACECAPS structure defines more driver surface capabilities in addition to those described in <a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a>.

## -struct-fields

### -field dwSize

Specifies the size of this DD_MORESURFACECAPS structure. The DD_MORESURFACECAPS structure is of variable size. There should be exactly <b>DD_HALINFO.vmiData.dwNumHeaps</b> copies of the <b>ddsExtendedHeapRestrictions</b> structure within the array member of this structure. The total size of a DD_MORESURFACECAPS structure is thus: 


```
dwSize = 
   sizeof(DD_MORESURFACECAPS) +
   (DD_HALINFO.vmiData.dwNumHeaps - 1) * sizeof(DDSCAPSEX) * 2
```


This calculation accounts for the minimum size of the DD_MORESURFACECAPS structure, which includes only one <b>ddsExtendedHeapRestrictions</b> array element. Any additional <b>ddsExtendedHeapRestrictions</b> array elements must be accounted for by adding the sizes of the remaining array elements. That is, by adding the product of the number of remaining <b>ddsExtendedHeapRestrictions</b> structures times the size of each one.

### -field ddsCapsMore

Specifies a DDSCAPSEX structure that provides the extensions to <b>ddcaps.ddsCaps</b> that describe the types of extended surfaces the driver can create. When a DDCAPS structure is returned to the application, it is a <a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a> structure manufactured from <b>DDCAPS.ddsCaps</b> and <b>DD_MORESURFACECAPS.ddsCapsMore</b>. A DDSCAPSEX structure is the same as a DDSCAPS2 structure without the <b>dwCaps</b> member.

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

<a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a>



<a href="/previous-versions/windows/hardware/drivers/ff550292(v=vs.85)">DDSCAPS2</a>