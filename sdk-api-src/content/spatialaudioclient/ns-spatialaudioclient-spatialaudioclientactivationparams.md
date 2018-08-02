---
UID: NS:spatialaudioclient.SpatialAudioClientActivationParams
title: SpatialAudioClientActivationParams
author: windows-sdk-content
description: Represents optional activation parameters for a spatial audio render stream. Pass this structure to ActivateAudioInterfaceAsync when activating an ISpatialAudioClient interface.
old-location: coreaudio\spatialaudioclientactivationparams.htm
old-project: CoreAudio
ms.assetid: 6FEC7A70-D12E-4DB9-91DC-A54D5CCF8B57
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: PSpatialAudioClientActivationParams, PSpatialAudioClientActivationParams structure pointer [Core Audio], SpatialAudioClientActivationParams, SpatialAudioClientActivationParams structure [Core Audio], coreaudio.spatialaudioclientactivationparams, spatialaudioclient/PSpatialAudioClientActivationParams, spatialaudioclient/SpatialAudioClientActivationParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: spatialaudioclient.h
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
req.typenames: SpatialAudioClientActivationParams
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudioclient.h
api_name:
 - SpatialAudioClientActivationParams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# SpatialAudioClientActivationParams structure


## -description


Represents optional activation parameters for a spatial audio render stream. Pass this structure to <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a> when activating an <a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a> interface.


## -struct-fields




### -field tracingContextId

An app-defined context identifier, used for event logging.


### -field appId

An identifier for the client app, used for event logging.



#### majorVersion

The major version number of the client app, used for event logging.



##### minorVersion1

The first minor version number of the client app, used for event logging.



###### minorVersion2

The second minor version number of the client app, used for event logging.



####### minorVersion3

The third minor version number of the client app, used for event logging.


### -field majorVersion

 


### -field minorVersion1

 


### -field minorVersion2

 


### -field minorVersion3

 




## -remarks



The following example code shows how to initialize this structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPVARIANT var; 
PropVariantInit(&amp;var);  
auto p = reinterpret_cast&lt;SpatialAudioClientActivationParams *&gt;(CoTaskMemAlloc(sizeof(SpatialAudioClientActivationParams)));  
if (nullptr == p) { ... } 
p-&gt;tracingContextId = /* context identifier */;  
p-&gt;appId = /* app identifier */;  
p-&gt;majorVersion = /* app version info */;  
p-&gt;majorVersionN = /* app version info */;
var.vt = VT_BLOB;
var.blob.cbSize = sizeof(*p);
var.blob.pBlobData = reinterpret_cast&lt;BYTE *&gt;(p); 
hr = ActivateAudioInterfaceAsync(device, __uuidof(ISpatialAudioClient), &amp;var, ...);
// ...
ropVariantClear(&amp;var);</pre>
</td>
</tr>
</table></span></div>
To access the <b>ActivateAudioIntefaceAsync</b>, you will need to link to mmdevapi.lib.



