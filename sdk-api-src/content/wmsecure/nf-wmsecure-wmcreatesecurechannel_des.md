---
UID: NF:wmsecure.WMCreateSecureChannel_DES
title: WMCreateSecureChannel_DES function
author: windows-driver-content
description: Creates an object that implements IWMSecureChannel.
old-location: wmformat\wmcreatesecurechannel_des.htm
old-project: wmformat
ms.assetid: d90e591f-82c0-4129-a810-8705d770dd3a
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WMCreateSecureChannel_DES, WMCreateSecureChannel_DES function [windows Media Format], wmformat.wmcreatesecurechannel_des, wmsecure/WMCreateSecureChannel_DES
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WMT_WATERMARK_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmsecure.h
api_name:
-	WMCreateSecureChannel_DES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateSecureChannel_DES function


## -description


Creates an object that implements <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>.


## -parameters




### -param ppChannel

Address of a pointer to the <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a> interface of the newly created secure channel object.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a>
 

 

