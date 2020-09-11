---
UID: NN:wsmandisp.IWSMan
title: IWSMan (wsmandisp.h)
description: Provides methods and properties used to create a session, represented by a Session object.
helpviewer_keywords: ["IWSMan","IWSMan interface [Windows Remote Management]","IWSMan interface [Windows Remote Management]","described","winrm.iwsman","wsmandisp/IWSMan"]
old-location: winrm\iwsman.htm
tech.root: winrm
ms.assetid: 4e5acfa6-9883-4716-ac69-92161c926c66
ms.date: 12/05/2018
ms.keywords: IWSMan, IWSMan interface [Windows Remote Management], IWSMan interface [Windows Remote Management],described, winrm.iwsman, wsmandisp/IWSMan
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSMan
 - wsmandisp/IWSMan
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSMan
 - IWSMan.CreateSession
 - IWSMan.CreateConnectionOptions
 - IWSMan.CommandLine
 - IWSMan.get_CommandLine
 - IWSMan.Error
 - IWSMan.get_Error
---

# IWSMan interface


## -description

Provides methods and properties used to create a session, represented by a <a href="https://docs.microsoft.com/windows/desktop/WinRM/session">Session</a> object. Any Windows Remote Management operations require creation of a <a href="https://docs.microsoft.com/windows/desktop/WinRM/session">Session</a> that connects to a remote computer, <a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-glossary">base management controller</a> (BMC), or the local computer. Operations include getting, writing, or enumerating data, or invoking methods.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSMan</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSMan</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWSMan</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateConnectionOptions</b></td>
<td align="left" width="63%">
Creates a,  <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanconnectionoptions">IWSManConnectionOptions</a> object that specifies the user name and password  used when  creating a remote session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>CreateSession</b></td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a> object that can then be used for subsequent network operations.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSMan</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>CommandLine</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the unprocessed command line for the current hosting process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">
<b>Error</b>

</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets error information.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinRM/wsman">WSMan</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRM/windows-remote-management-reference">Windows Remote Management Reference</a>

