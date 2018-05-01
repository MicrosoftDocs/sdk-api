---
UID: NF:mfmediaengine.IMFMediaEngineSrcElements.AddElement
title: IMFMediaEngineSrcElements::AddElement method
author: windows-driver-content
description: Adds a source element to the end of the list.
old-location: mf\imfmediaenginesrcelements_addelement.htm
old-project: medfound
ms.assetid: 2C98A70B-F6B3-4CA7-8D04-958DFCCD2A50
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: AddElement method [Media Foundation], AddElement method [Media Foundation], IMFMediaEngineSrcElements interface, AddElement,IMFMediaEngineSrcElements.AddElement, IMFMediaEngineSrcElements, IMFMediaEngineSrcElements interface [Media Foundation], AddElement method, IMFMediaEngineSrcElements::AddElement, mf.imfmediaenginesrcelements_addelement, mfmediaengine/IMFMediaEngineSrcElements::AddElement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineSrcElements.AddElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineSrcElements::AddElement method


## -description


Adds a source element to the end of the list.


## -parameters




### -param pURL [in]

The URL of the source element, or <b>NULL</b>.


### -param pType [in]

The MIME type of the source element, or <b>NULL</b>.


### -param pMedia [in]

A media-query string that specifies the intended media type, or <b>NULL</b>. If specified, the string should conform to the W3C <i>Media Queries</i> specification.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any of the parameters to this method can be <b>NULL</b>.

This method allocates copies of the <b>BSTR</b>s that are passed in.




## -see-also




<a href="https://msdn.microsoft.com/37A3EAC0-639C-47F3-AAB9-588EBEC8E1E3">IMFMediaEngineSrcElements</a>
 

 

