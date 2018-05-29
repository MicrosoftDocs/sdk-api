---
UID: NE:textstor.__MIDL___MIDL_itf_textstor_0000_0000_0002
title: "__MIDL___MIDL_itf_textstor_0000_0000_0002"
author: windows-sdk-content
description: Elements of the TsLayoutCode enumeration are used to specify the type of layout change in an ITextStoreACPSink::OnLayoutChange or ITextStoreAnchorSink::OnLayoutChange notification.
old-location: tsf\tslayoutcode.htm
old-project: TSF
ms.assetid: 879f83ba-211b-49f6-93b2-6cde5f50fc24
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: TS_LC_CHANGE, TS_LC_CREATE, TS_LC_DESTROY, TsLayoutCode, TsLayoutCode enumeration [Text Services Framework], __MIDL___MIDL_itf_textstor_0000_0000_0002, _tsf_tslayoutcode_ref, textstor/TS_LC_CHANGE, textstor/TS_LC_CREATE, textstor/TS_LC_DESTROY, textstor/TsLayoutCode, tsf.tslayoutcode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsLayoutCode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Textstor.h
api_name:
-	TsLayoutCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_textstor_0000_0000_0002 enumeration


## -description


Elements of the <b>TsLayoutCode</b> enumeration are used to specify the type of layout change in an <a href="https://msdn.microsoft.com/2018d3ef-892f-46c0-8dd0-3e27a9f2272c">ITextStoreACPSink::OnLayoutChange</a> or <a href="https://msdn.microsoft.com/22629ca6-5701-4f6f-b797-bb71c8d31da6">ITextStoreAnchorSink::OnLayoutChange</a> notification.


## -enum-fields




### -field TS_LC_CREATE

The view has just been created.


### -field TS_LC_CHANGE

The view layout has changed.


### -field TS_LC_DESTROY

The view is about to be destroyed.


## -see-also




<a href="https://msdn.microsoft.com/2018d3ef-892f-46c0-8dd0-3e27a9f2272c">ITextStoreACPSink::OnLayoutChange
      </a>



<a href="https://msdn.microsoft.com/22629ca6-5701-4f6f-b797-bb71c8d31da6">
        ITextStoreAnchorSink::OnLayoutChange
      </a>
 

 

