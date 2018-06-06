---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020
title: "__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020"
author: windows-sdk-content
description: This structure describes a dash element of a path.
old-location: xps\xps_dash.htm
old-project: printdocs
ms.assetid: c8f43f91-eefb-4025-8042-c2601e89d315
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: XPS_DASH, XPS_DASH structure [XPS Documents and Packaging], __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020, xps.xps_dash, xpsobjectmodel/XPS_DASH
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_DASH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_DASH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0020 structure


## -description


This structure describes a dash element of a path.


## -struct-fields




### -field length

Length of the visible segment of the dash element.


### -field gap

Length of the space between the visible segments of the dash sequence.


## -remarks



The length must be non-negative and is measured in multiples of the path's stroke thickness.

 Values of <b>length</b> do not include the end caps of the visible segments.

The shape of the end caps of the visible segments is determined by the <a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a> value.




## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/8c4d7314-71ad-4700-bc3e-f611e72c05df">XPS_DASH_CAP</a>
 

 

