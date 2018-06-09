---
UID: NF:wmsecure.WMCreateSecureChannel_Certified
title: WMCreateSecureChannel_Certified function
author: windows-sdk-content
description: Creates an object that implements IWMSecureChannel.
old-location: wmformat\wmcreatesecurechannel_certified.htm
old-project: wmformat
ms.assetid: 0381c653-05e1-417c-beee-40c4aa4271f4
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: WMCreateSecureChannel_Certified, WMCreateSecureChannel_Certified function [windows Media Format], wmformat.wmcreatesecurechannel_certified, wmsecure/WMCreateSecureChannel_Certified
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WMT_WATERMARK_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsecure.h
api_name:
 - WMCreateSecureChannel_Certified
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateSecureChannel_Certified function


## -description


Creates an object that implements <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>.


## -parameters




### -param ppChannel

Address of a pointer to the <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a> interface of the newly created secure channel object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

