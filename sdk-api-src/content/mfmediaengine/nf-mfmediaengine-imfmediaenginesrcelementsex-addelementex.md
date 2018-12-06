---
UID: NF:mfmediaengine.IMFMediaEngineSrcElementsEx.AddElementEx
title: IMFMediaEngineSrcElementsEx::AddElementEx
author: windows-sdk-content
description: Provides an enhanced version of IMFMediaEngineSrcElements::AddElement to add the key system intended to be used with content to an element.
old-location: mf\imfmediaenginesrcelementsex_addelementex.htm
tech.root: medfound
ms.assetid: ad799c61-3ffb-4879-a875-d218c0b56e1c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddElementEx, AddElementEx method [Media Foundation], AddElementEx method [Media Foundation],IMFMediaEngineSrcElementsEx interface, IMFMediaEngineSrcElementsEx interface [Media Foundation],AddElementEx method, IMFMediaEngineSrcElementsEx.AddElementEx, IMFMediaEngineSrcElementsEx::AddElementEx, mf.imfmediaenginesrcelementsex_addelementex, mfmediaengine/IMFMediaEngineSrcElementsEx::AddElementEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSrcElementsEx.AddElementEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineSrcElementsEx::AddElementEx


## -description


Provides an enhanced version of <a href="https://msdn.microsoft.com/2C98A70B-F6B3-4CA7-8D04-958DFCCD2A50">IMFMediaEngineSrcElements::AddElement</a> to add the key system intended to be used with content to an element.


## -parameters




### -param pURL

The URL of the source element, or <b>NULL</b>.


### -param pType

The MIME type of the source element, or <b>NULL</b>.


### -param pMedia

A media-query string that specifies the intended media type, or <b>NULL</b>. If specified, the string should conform to the W3C <i>Media Queries</i> specification.


### -param keySystem

The media key session.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f15cb527-0f46-4887-9e02-835f0115bc5b">IMFMediaEngineSrcElementsEx</a>
 

 

