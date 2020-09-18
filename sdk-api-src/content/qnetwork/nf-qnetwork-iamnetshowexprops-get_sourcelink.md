---
UID: NF:qnetwork.IAMNetShowExProps.get_SourceLink
title: IAMNetShowExProps::get_SourceLink (qnetwork.h)
description: The get_SourceLink method retrieves the source link.
helpviewer_keywords: ["IAMNetShowExProps interface [DirectShow]","get_SourceLink method","IAMNetShowExProps.get_SourceLink","IAMNetShowExProps::get_SourceLink","IAMNetShowExPropsget_SourceLink","dshow.iamnetshowexprops_get_sourcelink","get_SourceLink","get_SourceLink method [DirectShow]","get_SourceLink method [DirectShow]","IAMNetShowExProps interface","qnetwork/IAMNetShowExProps::get_SourceLink"]
old-location: dshow\iamnetshowexprops_get_sourcelink.htm
tech.root: dshow
ms.assetid: a5d79169-ae1b-4532-b367-ec2d24fae0b1
ms.date: 12/05/2018
ms.keywords: IAMNetShowExProps interface [DirectShow],get_SourceLink method, IAMNetShowExProps.get_SourceLink, IAMNetShowExProps::get_SourceLink, IAMNetShowExPropsget_SourceLink, dshow.iamnetshowexprops_get_sourcelink, get_SourceLink, get_SourceLink method [DirectShow], get_SourceLink method [DirectShow],IAMNetShowExProps interface, qnetwork/IAMNetShowExProps::get_SourceLink
req.header: qnetwork.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMNetShowExProps::get_SourceLink
 - qnetwork/IAMNetShowExProps::get_SourceLink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetShowExProps.get_SourceLink
---

# IAMNetShowExProps::get_SourceLink


## -description

The <code>get_SourceLink</code> method retrieves the source link.

## -parameters

### -param pbstrSourceLink

Pointer to a variable that receives the source link.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b>, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetshowexprops">IAMNetShowExProps Interface</a>