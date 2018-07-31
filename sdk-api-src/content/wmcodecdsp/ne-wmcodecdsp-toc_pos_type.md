---
UID: NE:wmcodecdsp.TOC_POS_TYPE
title: TOC_POS_TYPE
author: windows-sdk-content
description: The TOC_POS_TYPE enumeration contains members that specify the position type of a table of contents.
old-location: mf\toc_pos_type.htm
old-project: medfound
ms.assetid: 799059b5-9949-48af-8c54-4cb4975f8249
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: TOC_POS_INHEADER, TOC_POS_TOPLEVELOBJECT, TOC_POS_TYPE, TOC_POS_TYPE enumeration [Media Foundation], codecapi.toc_pos_type, mf.toc_pos_type, wmcodecdsp/TOC_POS_INHEADER, wmcodecdsp/TOC_POS_TOPLEVELOBJECT, wmcodecdsp/TOC_POS_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmcodecdsp.h
api_name:
 - TOC_POS_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TOC_POS_TYPE enumeration


## -description


The <b>TOC_POS_TYPE</b> enumeration contains members that specify the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of a table of contents.


## -enum-fields




### -field TOC_POS_INHEADER

Specifies that the table of contents is stored in the header of the media file.


### -field TOC_POS_TOPLEVELOBJECT

Specifies that the table of contents is stored in the body of the media file as a top level object.


## -remarks



Currently, only <b>TOC_POS_TOPLEVELOBJECT</b> is supported.




## -see-also




<a href="https://msdn.microsoft.com/d414c0d7-e3f1-4697-8ab1-f38815eaf889">Table of Contents Parser Enumerations</a>



<a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">The Position Type of a Table of Contents</a>
 

 

