---
UID: NF:wmp.IWMPError.webHelp
title: IWMPError::webHelp (wmp.h)
description: The webHelp method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).
helpviewer_keywords: ["IWMPError interface [Windows Media Player]","webHelp method","IWMPError.webHelp","IWMPError::webHelp","IWMPErrorwebHelp","webHelp","webHelp method [Windows Media Player]","webHelp method [Windows Media Player]","IWMPError interface","wmp.iwmperror_webhelp","wmp/IWMPError::webHelp"]
old-location: wmp\iwmperror_webhelp.htm
tech.root: WMP
ms.assetid: 98ece2f3-36c4-4bb2-9a06-c3ce57cbcbe7
ms.date: 4/26/2023
ms.keywords: IWMPError interface [Windows Media Player],webHelp method, IWMPError.webHelp, IWMPError::webHelp, IWMPErrorwebHelp, webHelp, webHelp method [Windows Media Player], webHelp method [Windows Media Player],IWMPError interface, wmp.iwmperror_webhelp, wmp/IWMPError::webHelp
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPError::webHelp
 - wmp/IWMPError::webHelp
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
 - IWMPError.webHelp
---

# IWMPError::webHelp


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>webHelp</b> method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

The Web Help pages always contain the latest and most detailed information about Windows Media Player errors. This method automatically transfers the other information needed by Web Help, such as the operating system version being used.

To access the Web Help pages directly, use the following error code and support center links.

<ul>
<li><a href="https://support.microsoft.com/windows/windows-media-player-errors-b3a9ccc1-6267-093e-0aa3-ea860644ecd4">Windows Media Player errors</a></li>
<li><a href="https://support.microsoft.com/ph/7763#tab0">Windows Media Player Solution Center</a></li>
</ul>
<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not launch the Windows Media Player Web Help page.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError Interface</a>
