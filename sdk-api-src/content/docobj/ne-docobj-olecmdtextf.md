---
UID: NE:docobj.OLECMDTEXTF
title: OLECMDTEXTF
author: windows-sdk-content
description: Specifies the type of information that an object should store in the OLECMDTEXT structure passed in IOleCommandTarget::QueryStatus.
old-location: com\olecmdtextf.htm
old-project: com
ms.assetid: 8978331a-33b6-4f57-b5a3-aae305c1d872
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OLECMDTEXTF, OLECMDTEXTF enumeration [COM], OLECMDTEXTF_NAME, OLECMDTEXTF_NONE, OLECMDTEXTF_STATUS, _ole_OLECMDTEXTF, com.olecmdtextf, docobj/OLECMDTEXTF, docobj/OLECMDTEXTF_NAME, docobj/OLECMDTEXTF_NONE, docobj/OLECMDTEXTF_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: docobj.h
req.include-header: 
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
tech.root: 
req.typenames: OLECMDTEXTF
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DocObj.h
api_name:
 - OLECMDTEXTF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# OLECMDTEXTF enumeration


## -description


Specifies the type of information that an object should store in the <a href="https://msdn.microsoft.com/c9552d2a-fb51-4d9f-acd5-32b3f20a9e1e">OLECMDTEXT</a> structure passed in <a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>. One value from this enumeration is stored the <b>cmdtextf</b> member of the <b>OLECMDTEXT</b> structure to indicate the desired information.




## -enum-fields




### -field OLECMDTEXTF_NONE

No extra information is requested.


### -field OLECMDTEXTF_NAME

The object should provide the localized name of the command.


### -field OLECMDTEXTF_STATUS

The object should provide a localized status string for the command.


## -see-also




<a href="https://msdn.microsoft.com/8acbf788-f113-43d9-800d-aad84db24498">IOleCommandTarget::QueryStatus</a>



<a href="https://msdn.microsoft.com/c9552d2a-fb51-4d9f-acd5-32b3f20a9e1e">OLECMDTEXT</a>
 

 

