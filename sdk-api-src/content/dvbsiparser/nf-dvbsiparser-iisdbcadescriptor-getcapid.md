---
UID: NF:dvbsiparser.IIsdbCADescriptor.GetCAPID
title: IIsdbCADescriptor::GetCAPID
author: windows-sdk-content
description: Gets the conditional access (CA) program identifier (PID) from a conditional access descriptor.
old-location: mstv\iisdbcadescriptor_getcapid.htm
old-project: mstv
ms.assetid: 9d4815f2-7f58-4952-a64b-067c99ae8d43
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCAPID, GetCAPID method [Microsoft TV Technologies], GetCAPID method [Microsoft TV Technologies],IIsdbCADescriptor interface, IIsdbCADescriptor interface [Microsoft TV Technologies],GetCAPID method, IIsdbCADescriptor.GetCAPID, IIsdbCADescriptor::GetCAPID, dvbsiparser/IIsdbCADescriptor::GetCAPID, mstv.iisdbcadescriptor_getcapid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbCADescriptor.GetCAPID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbCADescriptor::GetCAPID


## -description


Gets the conditional access (CA) program identifier (PID) from a conditional access descriptor. 


## -parameters




### -param pwVal [out]

Receives the conditional access PID value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6683f3db-636b-42bb-a46d-c175a4324023">IIsdbCADescriptor</a>
 

 

