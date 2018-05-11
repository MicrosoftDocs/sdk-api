---
UID: NF:mfidl.IMFNetCrossOriginSupport.GetSourceOrigin
title: IMFNetCrossOriginSupport::GetSourceOrigin
author: windows-driver-content
description: Returns the W3C origin of the HTML5 media element.
old-location: mf\imfnetcrossoriginsupport_getsourceorigin.htm
old-project: medfound
ms.assetid: 84379D86-DB03-4631-9A35-EFE9811B0D33
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetSourceOrigin, GetSourceOrigin method [Media Foundation], GetSourceOrigin method [Media Foundation],IMFNetCrossOriginSupport interface, IMFNetCrossOriginSupport interface [Media Foundation],GetSourceOrigin method, IMFNetCrossOriginSupport.GetSourceOrigin, IMFNetCrossOriginSupport::GetSourceOrigin, mf.imfnetcrossoriginsupport_getsourceorigin, mfidl/IMFNetCrossOriginSupport::GetSourceOrigin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFNetCrossOriginSupport.GetSourceOrigin
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetCrossOriginSupport::GetSourceOrigin


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Returns the W3C origin of the HTML5 media element.  


## -parameters




### -param wszSourceOrigin [out]

The W3C origin of the HTML5 media element.


## -returns



Returns S_OK upon successful completion.




## -remarks



Use <b>CoTaskMemFree</b> to free the string.




## -see-also




<a href="https://msdn.microsoft.com/239E5731-4425-46D4-AFEC-F3E59258B1DF">IMFNetCrossOriginSupport</a>
 

 

