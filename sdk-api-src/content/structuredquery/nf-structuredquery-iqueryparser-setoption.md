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

# IQueryParser::SetOption


## -description



          Sets a single option, such as a specified wordbreaker, for parsing an input string.


## -parameters




### -param option [in]

Type: <b><a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">STRUCTURED_QUERY_SINGLE_OPTION</a></b>


          Identifies the type of option to be set.
        


### -param pOptionValue [in]

Type: <b><a href="_stg_propvariant">PROPVARIANT</a>*</b>


          Pointer to a <a href="_stg_propvariant">PROPVARIANT</a> specifying the value to set for the <i>option</i> parameter. This value is interpreted differently depending on the value of the <i>option</i> parameter. 
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For more information, see <a href="https://msdn.microsoft.com/2753f0ad-2648-4ec2-b53f-089caad8ec15">STRUCTURED_QUERY_SINGLE_OPTION</a>.



