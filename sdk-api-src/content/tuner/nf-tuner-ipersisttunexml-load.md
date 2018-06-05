---
UID: NF:tuner.IPersistTuneXml.Load
title: IPersistTuneXml::Load
author: windows-sdk-content
description: Deserializes a tuning model object from an XML node.
old-location: mstv\ipersisttunexml_load.htm
old-project: mstv
ms.assetid: afbfb4da-ac61-496b-9383-05c312bbfc2c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPersistTuneXml interface [Microsoft TV Technologies],Load method, IPersistTuneXml.Load, IPersistTuneXml::Load, Load, Load method [Microsoft TV Technologies], Load method [Microsoft TV Technologies],IPersistTuneXml interface, mstv.ipersisttunexml_load, tuner/IPersistTuneXml::Load
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IPersistTuneXml.Load
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IPersistTuneXml::Load


## -description



      Deserializes a tuning model object from an XML node. 


## -parameters




### -param varValue [in]


            XML node used to deserialize the object. This parameter can be either a <b>BSTR</b> object or an <b>IXMLDOMNode</b> object.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2e08f727-9ffe-435b-9eca-4e9867fe410b">IPersistTuneXml</a>
 

 

