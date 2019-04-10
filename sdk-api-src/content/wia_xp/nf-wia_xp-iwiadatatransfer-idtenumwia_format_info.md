---
UID: NF:wia_xp.IWiaDataTransfer.idtEnumWIA_FORMAT_INFO
title: IWiaDataTransfer::idtEnumWIA_FORMAT_INFO (wia_xp.h)
author: windows-sdk-content
description: The IWiaDataTransfer::idtEnumWIA_FORMAT_INFO method creates a banded transfer implementation of the IEnumWIA_FORMAT_INFO interface.
old-location: wia\_wia_IWiaDataTransfer_idtEnumWIA_FORMAT_INFO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\idtenumwia_format_info.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaDataTransfer interface [WIA],idtEnumWIA_FORMAT_INFO method, IWiaDataTransfer.idtEnumWIA_FORMAT_INFO, IWiaDataTransfer::idtEnumWIA_FORMAT_INFO, _wia_IWiaDataTransfer_idtEnumWIA_FORMAT_INFO, idtEnumWIA_FORMAT_INFO, idtEnumWIA_FORMAT_INFO method [WIA], idtEnumWIA_FORMAT_INFO method [WIA],IWiaDataTransfer interface, wia._wia_IWiaDataTransfer_idtEnumWIA_FORMAT_INFO, wia_xp/IWiaDataTransfer::idtEnumWIA_FORMAT_INFO
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaDataTransfer.idtEnumWIA_FORMAT_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWiaDataTransfer::idtEnumWIA_FORMAT_INFO


## -description


The <b>IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</b> method creates a banded transfer implementation of the <a href="https://msdn.microsoft.com/en-us/library/ms630158(v=VS.85).aspx">IEnumWIA_FORMAT_INFO</a> interface.


## -parameters




### -param ppEnum [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms630158(v=VS.85).aspx">IEnumWIA_FORMAT_INFO</a>**</b>

Receives the address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms630158(v=VS.85).aspx">IEnumWIA_FORMAT_INFO</a> interface.


## -returns



Type: <b>HRESULT</b>

If it fails for any reason other than those specified in the following table, this method will return a standard COM error.

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>The <i>ppEnum</i> parameter is not the address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms630158(v=VS.85).aspx">IEnumWIA_FORMAT_INFO</a> interface.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is not enough memory to create the enumerator object.</td>
</tr>
<tr>
<td>S_OK</td>
<td>The enumerator object was successfully created.</td>
</tr>
</table>
 




## -remarks



This method creates the <a href="https://msdn.microsoft.com/en-us/library/ms630158(v=VS.85).aspx">IEnumWIA_FORMAT_INFO</a> interface that applications use to enumerate an array of <a href="https://msdn.microsoft.com/en-us/library/ms629878(v=VS.85).aspx">WIA_FORMAT_INFO</a> structures. This provides applications with the ability to determine the formats and media types of incoming data when transferring banded data.

Note that applications must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method on the interface pointers they receive through the <i>ppEnum</i> parameter.



