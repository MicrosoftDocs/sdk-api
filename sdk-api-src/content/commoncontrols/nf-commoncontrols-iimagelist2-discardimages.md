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

# IImageList2::DiscardImages


## -description


Discards images from list, as specified.


## -parameters




### -param iFirstImage [in]

Type: <b>int</b>

An index of first image to discard.


### -param iLastImage [in]

Type: <b>int</b>

An index of last image to discard.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Discard images flags. <b>ILDI_STANDBY</b> and <b>ILDI_PURGE</b> are mutually exclusive. <b>ILDI_RESETACCESS</b> can be combined with either. One or more of the following are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILDI_PURGE"></a><a id="ildi_purge"></a><dl>
<dt><b>ILDI_PURGE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Discard and purge. 

</td>
</tr>
<tr>
<td width="40%"><a id="ILDI_STANDBY"></a><a id="ildi_standby"></a><dl>
<dt><b>ILDI_STANDBY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Discard to standby list. 

</td>
</tr>
<tr>
<td width="40%"><a id="ILDI_RESETACCESS"></a><a id="ildi_resetaccess"></a><dl>
<dt><b>ILDI_RESETACCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Reset the "has been accessed" flag. 

</td>
</tr>
<tr>
<td width="40%"><a id="ILDI_QUERYACCESS"></a><a id="ildi_queryaccess"></a><dl>
<dt><b>ILDI_QUERYACCESS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Ask whether access flag is set (but do not reset). 

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



