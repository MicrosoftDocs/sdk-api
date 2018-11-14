---
UID: NN:mfidl.IMFSAMIStyle
title: IMFSAMIStyle
author: windows-sdk-content
description: Sets and retrieves Synchronized Accessible Media Interchange (SAMI) styles on the SAMI Media Source.
old-location: mf\imfsamistyle.htm
tech.root: medfound
ms.assetid: c4887c52-57af-4783-b853-11fe6ad3510e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSAMIStyle, IMFSAMIStyle interface [Media Foundation], IMFSAMIStyle interface [Media Foundation],described, c4887c52-57af-4783-b853-11fe6ad3510e, mf.imfsamistyle, mfidl/IMFSAMIStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFSAMIStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSAMIStyle interface


## -description


Sets and retrieves Synchronized Accessible Media Interchange (SAMI) styles on the <a href="https://msdn.microsoft.com/007c8181-089e-4e56-a31d-9d1942f90b07">SAMI Media Source</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSAMIStyle</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSAMIStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSAMIStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7501a4d5-eb5f-4f62-ae55-96ee999e561c">GetSelectedStyle</a>
</td>
<td align="left" width="63%">
Gets the current style from the SAMI media source.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/161cd457-9fab-4ebb-b8b8-f87326d67c66">GetStyleCount</a>
</td>
<td align="left" width="63%">
Gets the number of styles defined in the SAMI file.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0b183f0-8781-4fc5-97dd-e42b0e7bd5e5">GetStyles</a>
</td>
<td align="left" width="63%">
Gets a list of the style names defined in the SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7179756-517b-400b-8676-fd9ab5bbe74c">SetSelectedStyle</a>
</td>
<td align="left" width="63%">
Sets the current style on the SAMI media source.
        

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. The service identifier is <b>MF_SAMI_SERVICE</b>. Call <b>GetService</b> either directly on the SAMI media source, or on the Media Session (if you are using the SAMI source with the Media Session).




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/007c8181-089e-4e56-a31d-9d1942f90b07">SAMI Media Source</a>
 

 

