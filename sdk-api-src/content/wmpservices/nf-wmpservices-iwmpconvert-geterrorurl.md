---
UID: NF:wmpservices.IWMPConvert.GetErrorURL
title: IWMPConvert::GetErrorURL (wmpservices.h)
description: The GetErrorURL method is implemented by a conversion plug-in and called by Windows Media Player to retrieve the URL of a webpage that displays information to help the user correct the condition that caused an error.
helpviewer_keywords: ["GetErrorURL","GetErrorURL method [Windows Media Player]","GetErrorURL method [Windows Media Player]","IWMPConvert interface","IWMPConvert interface [Windows Media Player]","GetErrorURL method","IWMPConvert.GetErrorURL","IWMPConvert::GetErrorURL","IWMPConvertGetErrorURL","wmp.iwmpconvert_geterrorurl","wmpservices/IWMPConvert::GetErrorURL"]
old-location: wmp\iwmpconvert_geterrorurl.htm
tech.root: WMP
ms.assetid: 27a2ff9a-0c95-4c82-8e4a-c91d2a595005
ms.date: 12/05/2018
ms.keywords: GetErrorURL, GetErrorURL method [Windows Media Player], GetErrorURL method [Windows Media Player],IWMPConvert interface, IWMPConvert interface [Windows Media Player],GetErrorURL method, IWMPConvert.GetErrorURL, IWMPConvert::GetErrorURL, IWMPConvertGetErrorURL, wmp.iwmpconvert_geterrorurl, wmpservices/IWMPConvert::GetErrorURL
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player, build 10.00.00.4521 or later
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPConvert::GetErrorURL
 - wmpservices/IWMPConvert::GetErrorURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPConvert.GetErrorURL
---

# IWMPConvert::GetErrorURL


## -description

The <b>GetErrorURL</b> method is implemented by a conversion plug-in and called by Windows Media Player to retrieve the URL of a webpage that displays information to help the user correct the condition that caused an error.

## -parameters

### -param pbstrURL [out]

Pointer to a <b>BSTR</b> that receives the URL of the webpage that displays the error information.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

This is a synchronous call. Your code must complete and return as quickly as possible.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpconvert">IWMPConvert Interface</a>