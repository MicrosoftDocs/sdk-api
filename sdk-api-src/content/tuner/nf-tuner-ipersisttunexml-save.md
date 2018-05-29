---
UID: NF:tuner.IPersistTuneXml.Save
title: IPersistTuneXml::Save
author: windows-sdk-content
description: Serializes a tuning model object to an XML node.
old-location: mstv\ipersisttunexml_save.htm
old-project: mstv
ms.assetid: 5813966a-6053-43ce-9b92-e9552d9acdec
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPersistTuneXml interface [Microsoft TV Technologies],Save method, IPersistTuneXml.Save, IPersistTuneXml::Save, Save, Save method [Microsoft TV Technologies], Save method [Microsoft TV Technologies],IPersistTuneXml interface, mstv.ipersisttunexml_save, tuner/IPersistTuneXml::Save
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IPersistTuneXml.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IPersistTuneXml::Save


## -description


Serializes a tuning model object to an XML node.
          


## -parameters




### -param pvarFragment [out]


            Pointer to an <b>IXMLDOMNode</b> object that gets the data for the tuning model object.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2e08f727-9ffe-435b-9eca-4e9867fe410b">IPersistTuneXml</a>
 

 

