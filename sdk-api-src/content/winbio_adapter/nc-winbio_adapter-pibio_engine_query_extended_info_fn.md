---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN
title: PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN
author: windows-sdk-content
description: Determines the capabilities and limitations of the biometric engine component.
old-location: secbiomet\engineadapterqueryextendedinfo.htm
old-project: secbiomet
ms.assetid: 795547BF-FADE-4AFE-B5DF-1A295F759037
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: EngineAdapterQueryExtendedInfo, EngineAdapterQueryExtendedInfo callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN, PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN callback, secbiomet.engineadapterqueryextendedinfo, winbio_adapter/EngineAdapterQueryExtendedInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterQueryExtendedInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN callback function


## -description


Called by the Windows Biometric Framework to determine the capabilities and limitations of the biometric engine component.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param EngineInfo [out]

Pointer to the the <a href="https://msdn.microsoft.com/83586E04-24CA-4A39-836F-C80DB1508C71">WINBIO_EXTENDED_ENGINE_INFO</a> structure that contains the engine information returned by this function.


### -param EngineInfoSize [in]

The specified size in bytes of the engine information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> and <i>EngineInfo</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>EngineInfoSize</i> value is less than the size needed to return the engine information.

</td>
</tr>
</table>
 




## -remarks



This method is called once during configuration of the biometric unit. 

It will also be called if a client application uses the <a href="https://msdn.microsoft.com/63e38e74-3d46-4474-a31c-eaf724156bc6">WinBioGetProperty</a> function to query the value of the <b>WINBIO_PROPERTY_EXTENDED_ENGINE_INFO</b> property.



