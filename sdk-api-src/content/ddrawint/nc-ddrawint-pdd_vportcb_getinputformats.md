---
UID: NC:ddrawint.PDD_VPORTCB_GETINPUTFORMATS
title: PDD_VPORTCB_GETINPUTFORMATS (ddrawint.h)
description: The DdVideoPortGetInputFormats callback function determines the input formats that the DirectDraw VPE object can accept.
helpviewer_keywords: ["DdVideoPortGetInputFormats","DdVideoPortGetInputFormats callback function [Display Devices]","PDD_VPORTCB_GETINPUTFORMATS","PDD_VPORTCB_GETINPUTFORMATS callback","ddfncs_0dc8b987-a259-4778-8cbc-1fbb7a1169bd.xml","ddrawint/DdVideoPortGetInputFormats","display.ddvideoportgetinputformats"]
old-location: display\ddvideoportgetinputformats.htm
tech.root: display
ms.assetid: aac34116-a6a2-4d00-b0c4-87fac786b68d
ms.date: 12/05/2018
ms.keywords: DdVideoPortGetInputFormats, DdVideoPortGetInputFormats callback function [Display Devices], PDD_VPORTCB_GETINPUTFORMATS, PDD_VPORTCB_GETINPUTFORMATS callback, ddfncs_0dc8b987-a259-4778-8cbc-1fbb7a1169bd.xml, ddrawint/DdVideoPortGetInputFormats, display.ddvideoportgetinputformats
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_VPORTCB_GETINPUTFORMATS
 - ddrawint/PDD_VPORTCB_GETINPUTFORMATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortGetInputFormats
---

## -description

The <b>DdVideoPortGetInputFormats</b> callback function determines the input formats that the DirectDraw VPE object can accept.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportinputformatdata">DD_GETVPORTINPUTFORMATDATA</a> structure that contains the information required for the driver to return the input formats the VPE object can accept.

## -returns

<b>DdVideoPortGetInputFormats</b> returns one of the following callback codes:

## -remarks

<b>DdVideoPortGetInputFormats</b> must be implemented in DirectDraw drivers that support VPE.

DirectDraw calls <b>DdVideoPortGetInputFormats</b> to obtain the number of input formats supported by the specified VPE object and a description of each format. <b>DdVideoPortGetInputFormats</b> is called twice for the specified VPE object:

<ul>
<li>
In the first call, the <b>lpddpfFormat</b> member of the DD_GETVPORTINPUTFORMATDATA structure at <i>lpGetInputFormats</i> is <b>NULL</b>. The driver should write the number of input formats that the VPE object supports in the <b>dwNumFormats</b> member of DD_GETVPORTINPUTFORMATDATA. Upon return, DirectDraw will allocate this number of <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structures to pass in the second call to <b>DdVideoPortGetInputFormats</b>.

</li>
<li>
In the second call, <b>lpddpfFormat</b> points to the array of allocated DDPIXELFORMAT structures. The driver should fill in each structure to describe each input format that the VPE object supports. The driver should also return the number of supported input formats in <b>dwNumFormats</b>. Note that the driver is guaranteed that the buffer to which <b>lpddpfFormat</b> points is large enough to hold the format information being requested.

</li>
</ul>
If the <b>dwFlags</b> member of the DD_GETVPORTINPUTFORMATDATA structure is set only to DDVPFORMAT_VIDEO, the driver should return only those formats that are supported for the normal video data. If <b>dwFlags</b> is set only to DDVPFORMAT_VBI, the driver should return only those formats supported for the <a href="/windows-hardware/drivers/">VBI</a> data. If <b>dwFlags</b> is set to both flags, the driver should return all formats supported by the VPE object.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportinputformatdata">DD_GETVPORTINPUTFORMATDATA</a>