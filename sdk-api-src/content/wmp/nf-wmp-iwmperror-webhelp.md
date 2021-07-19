---
UID: NF:wmp.IWMPError.webHelp
title: IWMPError::webHelp (wmp.h)
description: The webHelp method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).
helpviewer_keywords: ["IWMPError interface [Windows Media Player]","webHelp method","IWMPError.webHelp","IWMPError::webHelp","IWMPErrorwebHelp","webHelp","webHelp method [Windows Media Player]","webHelp method [Windows Media Player]","IWMPError interface","wmp.iwmperror_webhelp","wmp/IWMPError::webHelp"]
old-location: wmp\iwmperror_webhelp.htm
tech.root: WMP
ms.assetid: 98ece2f3-36c4-4bb2-9a06-c3ce57cbcbe7
ms.date: 12/05/2018
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
<li><a href="https://support.microsoft.com/help/886273">Windows Media Player Error Code Information</a></li>
<li><a href="https://support.microsoft.com/ph/7763#tab0">Windows Media Player Solution Center</a></li>
</ul>
<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not launch the Windows Media Player Web Help page.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError Interface</a>
