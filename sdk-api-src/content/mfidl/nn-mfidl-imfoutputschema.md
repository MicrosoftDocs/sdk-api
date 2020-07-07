---
UID: NN:mfidl.IMFOutputSchema
title: IMFOutputSchema (mfidl.h)
description: Encapsulates information about an output protection system and its corresponding configuration data.
helpviewer_keywords: ["IMFOutputSchema","IMFOutputSchema interface [Media Foundation]","IMFOutputSchema interface [Media Foundation]","described","d0786628-dde9-43a9-8e81-0b0c396ad426","mf.imfoutputschema","mfidl/IMFOutputSchema"]
old-location: mf\imfoutputschema.htm
tech.root: medfound
ms.assetid: d0786628-dde9-43a9-8e81-0b0c396ad426
ms.date: 12/05/2018
ms.keywords: IMFOutputSchema, IMFOutputSchema interface [Media Foundation], IMFOutputSchema interface [Media Foundation],described, d0786628-dde9-43a9-8e81-0b0c396ad426, mf.imfoutputschema, mfidl/IMFOutputSchema
f1_keywords:
- mfidl/IMFOutputSchema
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFOutputSchema
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFOutputSchema interface


## -description


Encapsulates information about an output protection system and its corresponding configuration data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFOutputSchema</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFOutputSchema</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFOutputSchema</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata">GetConfigurationData</a>
</td>
<td align="left" width="63%">
Returns configuration data for the output protection system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputschema-getoriginatorid">GetOriginatorID</a>
</td>
<td align="left" width="63%">
Retrieives a GUID identifying the input trust authority (ITA) that generated this output schema object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputschema-getschematype">GetSchemaType</a>
</td>
<td align="left" width="63%">
Retrieves the output protection system that is represented by this object.

</td>
</tr>
</table> 


## -remarks



If the configuration information for the output protection system does not require more than a <b>DWORD</b> of space, the configuration information is retrieved in the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata">GetConfigurationData</a> method. If more than a <b>DWORD</b> of configuration information is needed, it is stored using the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

