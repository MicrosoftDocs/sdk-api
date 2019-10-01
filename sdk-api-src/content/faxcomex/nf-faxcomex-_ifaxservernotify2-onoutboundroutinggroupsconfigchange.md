---
UID: NF:faxcomex._IFaxServerNotify2.OnOutboundRoutingGroupsConfigChange
title: _IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange (faxcomex.h)
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange method when there is a configuration change related to outbound fax routing groups.
old-location: fax\_mfax_ifaxservernotify2_onoutboundroutinggroupsconfigchange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onoutboundroutinggroupsconfigchange.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnOutboundRoutingGroupsConfigChange method, IFaxServerNotify2.OnOutboundRoutingGroupsConfigChange, IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange, OnOutboundRoutingGroupsConfigChange, OnOutboundRoutingGroupsConfigChange method [Fax Service], OnOutboundRoutingGroupsConfigChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnOutboundRoutingGroupsConfigChange, _IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange, _mfax_ifaxservernotify2_onoutboundroutinggroupsconfigchange, fax._mfax_ifaxservernotify2_onoutboundroutinggroupsconfigchange, faxcomex/IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxServerNotify2.OnOutboundRoutingGroupsConfigChange"
req.header: faxcomex.h
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServerNotify2.OnOutboundRoutingGroupsConfigChange
 - IFaxServerNotify2.OnOutboundRoutingGroupsConfigChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange


## -description


The fax service calls the <b>IFaxServerNotify2::OnOutboundRoutingGroupsConfigChange</b> method when there is a configuration change related to outbound fax routing groups.


## -parameters




### -param pFaxServer

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a>*</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-registering-for-fax-events">Registering for Fax Events</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a>
 

 

