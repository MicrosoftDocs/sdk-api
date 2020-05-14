---
UID: NF:wmsecure.WMCreateSecureChannel_Certified
title: WMCreateSecureChannel_Certified function (wmsecure.h)
description: Creates an object that implements IWMSecureChannel.helpviewer_keywords: ["WMCreateSecureChannel_Certified","WMCreateSecureChannel_Certified function [windows Media Format]","wmformat.wmcreatesecurechannel_certified","wmsecure/WMCreateSecureChannel_Certified"]
old-location: wmformat\wmcreatesecurechannel_certified.htm
tech.root: wmformat
ms.assetid: 0381c653-05e1-417c-beee-40c4aa4271f4
ms.date: 12/05/2018
ms.keywords: WMCreateSecureChannel_Certified, WMCreateSecureChannel_Certified function [windows Media Format], wmformat.wmcreatesecurechannel_certified, wmsecure/WMCreateSecureChannel_Certified
f1_keywords:
- wmsecure/WMCreateSecureChannel_Certified
dev_langs:
- c++
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wmsecure.h
api_name:
- WMCreateSecureChannel_Certified
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateSecureChannel_Certified function


## -description


Creates an object that implements <a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>.


## -parameters




### -param ppChannel

Address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface of the newly created secure channel object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a>
 

 

