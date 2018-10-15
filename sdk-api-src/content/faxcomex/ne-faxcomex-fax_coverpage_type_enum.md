---
UID: NE:faxcomex.FAX_COVERPAGE_TYPE_ENUM
title: FAX_COVERPAGE_TYPE_ENUM
author: windows-sdk-content
description: The FAX_COVERPAGE_TYPE_ENUM enumeration defines whether a cover page template file is a local computer cover page or a server-based cover page. It can also specify that no file is used.
old-location: fax\_mfax_fax_coverpage_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7lm5.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: FAX_COVERPAGE_TYPE_ENUM, FAX_COVERPAGE_TYPE_ENUM enumeration [Fax Service], _mfax_fax_coverpage_type_enum, fax._mfax_fax_coverpage_type_enum, faxcomex/FAX_COVERPAGE_TYPE_ENUM, faxcomex/fcptLOCAL, faxcomex/fcptNONE, faxcomex/fcptSERVER, fcptLOCAL, fcptNONE, fcptSERVER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - FaxComex.h
api_name:
 - FAX_COVERPAGE_TYPE_ENUM
product: Windows
targetos: Windows
req.typenames: FAX_COVERPAGE_TYPE_ENUM
req.redist: 
---

# FAX_COVERPAGE_TYPE_ENUM enumeration


## -description


The <b>FAX_COVERPAGE_TYPE_ENUM</b> enumeration defines whether a cover page template file is a local computer cover page or a server-based cover page. It can also specify that no file is used. 


## -enum-fields




### -field fcptNONE

No cover page.


### -field fcptLOCAL

Use a cover page from local computer.


### -field fcptSERVER

Use a cover page from the fax server common coverpages folder. 


## -see-also




<a href="https://msdn.microsoft.com/ca6b43c6-7b06-448c-b715-3c92a5c4a853">IFaxDocument::get_CoverPageType</a>
 

 

