---
UID: NF:tapi3if.ITLegacyWaveSupport.IsFullDuplex
title: ITLegacyWaveSupport::IsFullDuplex (tapi3if.h)
author: windows-sdk-content
description: The IsFullDuplex method gets an indicator of whether the address supports wave devices.
old-location: tapi3\itlegacywavesupport_isfullduplex.htm
tech.root: Tapi
ms.assetid: 117586d7-8214-4fc8-9c7d-08865582cc2a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITLegacyWaveSupport interface [TAPI 2.2],IsFullDuplex method, ITLegacyWaveSupport.IsFullDuplex, ITLegacyWaveSupport::IsFullDuplex, IsFullDuplex, IsFullDuplex method [TAPI 2.2], IsFullDuplex method [TAPI 2.2],ITLegacyWaveSupport interface, _tapi3_itlegacywavesupport_isfullduplex, tapi3.itlegacywavesupport_isfullduplex, tapi3if/ITLegacyWaveSupport::IsFullDuplex
ms.topic: method
f1_keywords: ["tapi3if/ITLegacyWaveSupport.IsFullDuplex"]
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyWaveSupport.IsFullDuplex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITLegacyWaveSupport::IsFullDuplex


## -description


The 
<b>IsFullDuplex</b> method gets an indicator of whether the address supports wave devices.


## -parameters




### -param pSupport

Pointer to 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-fullduplex_support">FULLDUPLEX_SUPPORT</a> enumerator member, such as FDS_SUPPORTED.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-fullduplex_support">FULLDUPLEX_SUPPORT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport">ITLegacyWaveSupport</a>
 

 

