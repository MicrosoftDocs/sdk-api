---
UID: NE:faxcomex.FAX_PRIORITY_TYPE_ENUM
title: FAX_PRIORITY_TYPE_ENUM
author: windows-sdk-content
description: The FAX_PRIORITY_TYPE_ENUM enumeration defines the types of priorities for outbound faxes.
old-location: fax\_mfax_fax_priority_type_enum.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_5oz1.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FAX_PRIORITY_TYPE_ENUM, FAX_PRIORITY_TYPE_ENUM enumeration [Fax Service], _mfax_fax_priority_type_enum, fax._mfax_fax_priority_type_enum, faxcomex/FAX_PRIORITY_TYPE_ENUM, faxcomex/fptHIGH, faxcomex/fptLOW, faxcomex/fptNORMAL, fptHIGH, fptLOW, fptNORMAL
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FAX_PRIORITY_TYPE_ENUM
product: Windows
targetos: Windows
req.typenames: FAX_PRIORITY_TYPE_ENUM
req.redist: 
---

# FAX_PRIORITY_TYPE_ENUM enumeration


## -description


The <b>FAX_PRIORITY_TYPE_ENUM</b> enumeration defines the types of priorities for outbound faxes.


## -enum-fields




### -field fptLOW

The fax will be sent with a low priority. All faxes that have a normal or a high priority will be sent before a fax that has a low priority.


### -field fptNORMAL

The fax will be sent with a normal priority. All faxes that have a high priority will be sent before a fax that has a normal priority.


### -field fptHIGH

The fax will be sent with a high priority.


## -see-also




<a href="https://msdn.microsoft.com/4f7ebcad-ff7d-4c11-b4c4-c7325415231e">IFaxDocument::get_Priority</a>



<a href="https://msdn.microsoft.com/0cf5d46f-0c26-4fa5-808e-13bdf1901964">IFaxOutgoingJob::get_Priority</a>



<a href="https://msdn.microsoft.com/bd727334-0e7a-4f2b-a4bb-2308c9ecfc9a">IFaxOutgoingMessage::get_Priority</a>
 

 

