---
UID: NF:faxcom.IFaxStatus.Refresh
title: IFaxStatus::Refresh
author: windows-sdk-content
description: The Refresh method updates FaxStatus object information for the associated parent FaxPort object.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_53c8.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxStatus interface [Fax Service],Refresh method, IFaxStatus.Refresh, IFaxStatus::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_refresh, fax._mfax_ifaxstatus_mfax_ifaxstatus_refresh_cpp, fax._mfax_ifaxstatus_refresh, faxcom/IFaxStatus::Refresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxStatus.Refresh
 - IFaxStatus.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::Refresh


## -description


The <b>Refresh</b> method updates <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object information for the associated parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <b>IFaxStatus::Refresh</b> method to update the information for a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object. An application must call this method to poll a fax port for new status information. After you successfully call <b>IFaxStatus::Refresh</b>, you must call the appropriate <a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a> interface method to retrieve new attribute values that are valid.

It is recommended that you limit calls to this method because frequent calls to <b>IFaxStatus::Refresh</b> can affect system performance.




## -see-also




<a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a>
 

 

