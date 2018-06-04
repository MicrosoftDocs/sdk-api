---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IImageList::GetItemFlags


## -description


Gets the flags of an image.


## -parameters




### -param i [in]

Type: <b>int</b>

A value of type <b>int</b> that contains the index of the images whose flags need to be retrieved.


### -param dwFlags [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

A pointer to a <b>DWORD</b> that contains the flags when the method returns. One of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILIF_ALPHA"></a><a id="ilif_alpha"></a><dl>
<dt><b>ILIF_ALPHA</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that the item in the imagelist has an alpha channel.

</td>
</tr>
<tr>
<td width="40%"><a id="ILIF_LOWQUALITY"></a><a id="ilif_lowquality"></a><dl>
<dt><b>ILIF_LOWQUALITY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later.</b> Indicates that the item in the imagelist was generated via a StretchBlt function, consequently image quality may have degraded.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use <b>IImageList::GetItemFlags</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



