---
UID: NF:commoncontrols.IImageList2.DiscardImages
title: IImageList2::DiscardImages (commoncontrols.h)
description: Discards images from list, as specified.
helpviewer_keywords: ["DiscardImages","DiscardImages method [Windows Controls]","DiscardImages method [Windows Controls]","IImageList2 interface","IImageList2 interface [Windows Controls]","DiscardImages method","IImageList2.DiscardImages","IImageList2::DiscardImages","ILDI_PURGE","ILDI_QUERYACCESS","ILDI_RESETACCESS","ILDI_STANDBY","_shell_IImageList2_DiscardImages","_shell_IImageList2_DiscardImages_cpp","commoncontrols/IImageList2::DiscardImages","controls.IImageList2_DiscardImages","controls._shell_IImageList2_DiscardImages"]
old-location: controls\IImageList2_DiscardImages.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist2\discardimages.htm
ms.date: 12/05/2018
ms.keywords: DiscardImages, DiscardImages method [Windows Controls], DiscardImages method [Windows Controls],IImageList2 interface, IImageList2 interface [Windows Controls],DiscardImages method, IImageList2.DiscardImages, IImageList2::DiscardImages, ILDI_PURGE, ILDI_QUERYACCESS, ILDI_RESETACCESS, ILDI_STANDBY, _shell_IImageList2_DiscardImages, _shell_IImageList2_DiscardImages_cpp, commoncontrols/IImageList2::DiscardImages, controls.IImageList2_DiscardImages, controls._shell_IImageList2_DiscardImages
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Commoncontrols.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IImageList2::DiscardImages
 - commoncontrols/IImageList2::DiscardImages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList2.DiscardImages
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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.