---
UID: NC:ddrawint.PDD_VPORTCB_GETVPORTCONNECT
title: PDD_VPORTCB_GETVPORTCONNECT (ddrawint.h)
description: The DdVideoPortGetConnectInfo callback function returns the connections supported by the specified VPE object.
helpviewer_keywords: ["DdVideoPortGetConnectInfo","DdVideoPortGetConnectInfo callback function [Display Devices]","PDD_VPORTCB_GETVPORTCONNECT","PDD_VPORTCB_GETVPORTCONNECT callback","ddfncs_10f9e183-b3f5-42c4-b97a-c44f8b5ea791.xml","ddrawint/DdVideoPortGetConnectInfo","display.ddvideoportgetconnectinfo"]
old-location: display\ddvideoportgetconnectinfo.htm
tech.root: display
ms.assetid: b6be5f94-6d4d-4f7a-a8d9-15bfc7a15d3b
ms.date: 12/05/2018
ms.keywords: DdVideoPortGetConnectInfo, DdVideoPortGetConnectInfo callback function [Display Devices], PDD_VPORTCB_GETVPORTCONNECT, PDD_VPORTCB_GETVPORTCONNECT callback, ddfncs_10f9e183-b3f5-42c4-b97a-c44f8b5ea791.xml, ddrawint/DdVideoPortGetConnectInfo, display.ddvideoportgetconnectinfo
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
 - PDD_VPORTCB_GETVPORTCONNECT
 - ddrawint/PDD_VPORTCB_GETVPORTCONNECT
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
 - DdVideoPortGetConnectInfo
---

## -description

The <i>DdVideoPortGetConnectInfo</i> callback function returns the connections supported by the specified VPE object.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportconnectdata">DD_GETVPORTCONNECTDATA</a> structure that contains the information required for the driver to return the VPE object connection data.

## -returns

<i>DdVideoPortGetConnectInfo</i> returns one of the following callback codes:

## -remarks

<i>DdVideoPortGetConnectInfo</i> must be implemented in DirectDraw drivers that support VPE.

DirectDraw calls <i>DdVideoPortGetConnectInfo</i> to obtain the number of connections supported by the specified VPE object and the characteristics of each connection. <i>DdVideoPortGetConnectInfo</i> is called twice for the specified VPE object:

<ul>
<li>
In the first call, the <b>lpConnect</b> member of the DD_GETVPORTCONNECTDATA structure at <i>lpGetConnect</i> is <b>NULL</b>. The driver should write the number of connections that the VPE object supports in the <b>dwNumEntries</b> member of DD_GETVPORTCONNECTDATA. Upon return, DirectDraw will allocate this number of DDVIDEOPORTCONNECT structures to pass in the second call to <i>DdVideoPortGetConnectInfo</i>.

</li>
<li>
In the second call, <b>lpConnect</b> points to the array of allocated <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddvideoportconnect">DDVIDEOPORTCONNECT</a> structures. The driver should fill in each structure to describe each connection that the VPE object supports. The driver should also return the number of supported connections in <b>dwNumEntries</b>. Note that the driver is guaranteed that the buffer to which <b>lpConnect</b> points is large enough to hold the connection information being requested.

</li>
</ul>

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddvideoportconnect">DDVIDEOPORTCONNECT</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportconnectdata">DD_GETVPORTCONNECTDATA</a>