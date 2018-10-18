---
UID: NF:commoncontrols.IImageList.GetItemFlags
title: IImageList::GetItemFlags
author: windows-sdk-content
description: Gets the flags of an image.
old-location: controls\IImageList_GetItemFlags.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\getitemflags.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetItemFlags, GetItemFlags method [Windows Controls], GetItemFlags method [Windows Controls],IImageList interface, IImageList interface [Windows Controls],GetItemFlags method, IImageList.GetItemFlags, IImageList::GetItemFlags, ILIF_ALPHA, ILIF_LOWQUALITY, comctl_IImageList_GetItemFlags, comctl_IImageList_GetItemFlags_cpp, commoncontrols/IImageList::GetItemFlags, controls.IImageList_GetItemFlags, controls.comctl_IImageList_GetItemFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList.GetItemFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



To use <b>IImageList::GetItemFlags</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>. 



