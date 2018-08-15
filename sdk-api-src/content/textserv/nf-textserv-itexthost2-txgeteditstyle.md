---
UID: NF:textserv.ITextHost2.TxGetEditStyle
title: ITextHost2::TxGetEditStyle
author: windows-sdk-content
description: Gets whether a rich edit control is in a dialog box.
old-location: controls\itexthost2_txgeteditstyle.htm
old-project: controls
ms.assetid: 8C5468C9-D152-4F57-9E8A-23B4852BFD69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetEditStyle method, ITextHost2.TxGetEditStyle, ITextHost2::TxGetEditStyle, TXES_ISDIALOG, TxGetEditStyle, TxGetEditStyle method [Windows Controls], TxGetEditStyle method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgeteditstyle, textserv/ITextHost2::TxGetEditStyle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextHost2.TxGetEditStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost2::TxGetEditStyle


## -description


Gets whether a rich edit control is in a dialog box.


## -parameters




### -param dwItem

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Mask that indicates the edit style flags to retrieve. It can be the following value.  

<a id="TXES_ISDIALOG"></a>
<a id="txes_isdialog"></a>


#### TXES_ISDIALOG


### -param pdwData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXES_ISDIALOG"></a><a id="txes_isdialog"></a><dl>
<dt><b>TXES_ISDIALOG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the host of the rich edit control is a dialog box.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A715E70C-E8BB-4796-BDA6-90B745EC7761">ITextHost2</a>
 

 

