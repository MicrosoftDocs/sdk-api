---
UID: NF:wmp.IWMPEvents.DomainChange
title: IWMPEvents::DomainChange (wmp.h)
description: The DomainChange event occurs when the DVD domain changes.
helpviewer_keywords: ["DomainChange","DomainChange method [Windows Media Player]","DomainChange method [Windows Media Player]","IWMPEvents interface","IWMPEvents interface [Windows Media Player]","DomainChange method","IWMPEvents.DomainChange","IWMPEvents::DomainChange","IWMPEventsDomainChange","wmp.iwmpevents_iwmpevents__domainchange","wmp/IWMPEvents::DomainChange"]
old-location: wmp\iwmpevents_iwmpevents__domainchange.htm
tech.root: WMP
ms.assetid: deb8e05e-a6dc-4971-9c34-9c12f1dedc9e
ms.date: 4/26/2023
ms.keywords: DomainChange, DomainChange method [Windows Media Player], DomainChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],DomainChange method, IWMPEvents.DomainChange, IWMPEvents::DomainChange, IWMPEventsDomainChange, wmp.iwmpevents_iwmpevents__domainchange, wmp/IWMPEvents::DomainChange
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents::DomainChange
 - wmp/IWMPEvents::DomainChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents.DomainChange
---

# IWMPEvents::DomainChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DomainChange</b> event occurs when the DVD domain changes.

## -parameters

### -param strDomain [in]

Specifies the new domain. It can be one of the following values:

<table>
<tr>
<th>String</th>
<th>Description</th>
</tr>
<tr>
<td>firstPlay</td>
<td>Performing default initialization of a DVD disc.</td>
</tr>
<tr>
<td>videoManagerMenu</td>
<td>Displaying menus for whole disc. Also known as Root Menu or topMenu.</td>
</tr>
<tr>
<td>videoTitleSetMenu</td>
<td>Displaying menus for current title set. Also known as titleMenu</td>
</tr>
<tr>
<td>title</td>
<td>Displaying the current title.</td>
</tr>
<tr>
<td>stop</td>
<td>The DVD Navigator is in the DVD Stop domain.</td>
</tr>
</table>

## -remarks

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

Windows XP or later.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>