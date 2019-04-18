---
UID: NC:ddrawint.PDD_VPORTCB_CANCREATEVIDEOPORT
title: PDD_VPORTCB_CANCREATEVIDEOPORT (ddrawint.h)
author: windows-sdk-content
description: The DdVideoPortCanCreate callback function determines whether the driver can support a DirectDraw VPE object of the specified description.
old-location: display\ddvideoportcancreate.htm
tech.root: display
ms.assetid: 742c7af2-0611-4cca-b18c-e14b18068d7e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DdVideoPortCanCreate, DdVideoPortCanCreate callback function [Display Devices], PDD_VPORTCB_CANCREATEVIDEOPORT, PDD_VPORTCB_CANCREATEVIDEOPORT callback, ddfncs_dfe3285f-627c-4f0d-b7e7-ffd87d88fe46.xml, ddrawint/DdVideoPortCanCreate, display.ddvideoportcancreate
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdVideoPortCanCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_VPORTCB_CANCREATEVIDEOPORT callback function


## -description


The <i>DdVideoPortCanCreate</i> callback function determines whether the driver can support a DirectDraw VPE object of the specified description.


## -parameters




### -param Arg1








#### - lpCanCreateVideoPort

Points to a <a href="https://msdn.microsoft.com/60116f1d-fca2-4282-95a9-2af8da113a20">DD_CANCREATEVPORTDATA</a> structure that contains the information necessary for the driver to determine whether the specified DirectDraw VPE object can be supported.


## -returns



<i>DdVideoPortCanCreate</i> returns one of the following callback codes:




## -remarks



<i>DdVideoPortCanCreate</i> must be implemented in drivers that support VPE.

The driver should check the members of the <a href="https://msdn.microsoft.com/efd5907c-ed75-40be-b568-7c305310f79b">DDVIDEOPORTDESC</a> structure to which the <b>lpDDVideoPortDesc</b> member of the DD_CANCREATEVPORTDATA structure at <i>lpCanCreateVideoPort</i> points to determine whether the hardware supports the specified type of VPE object.




## -see-also




<a href="https://msdn.microsoft.com/efd5907c-ed75-40be-b568-7c305310f79b">DDVIDEOPORTDESC</a>



<a href="https://msdn.microsoft.com/60116f1d-fca2-4282-95a9-2af8da113a20">DD_CANCREATEVPORTDATA</a>



<a href="https://msdn.microsoft.com/eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7">DdVideoPortCreate</a>
 

 

