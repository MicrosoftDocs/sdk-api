---
UID: NF:winsync.IProviderConverter.Initialize
title: IProviderConverter::Initialize
author: windows-sdk-content
description: When implemented by a derived class, initializes the IProviderConverter object with the ISyncProvider object to be converted to IKnowledgeSyncProvider.
old-location: winsync\iproviderconverter_initialize.htm
old-project: winsync
ms.assetid: 5bdb8b16-cda3-4f0d-b147-4dcfce81f592
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IProviderConverter interface [Windows Sync],Initialize method, IProviderConverter.Initialize, IProviderConverter::Initialize, Initialize, Initialize method [Windows Sync], Initialize method [Windows Sync],IProviderConverter interface, winsync.iproviderconverter_initialize, winsync/IProviderConverter::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IProviderConverter.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IProviderConverter::Initialize


## -description


When implemented by a derived class, initializes the <b>IProviderConverter</b> object with the <b>ISyncProvider</b> object to be converted to <b>IKnowledgeSyncProvider</b>.


## -parameters




### -param pISyncProvider [in]

The <b>ISyncProvider</b> object to be converted.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>Converter-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/67dc6290-00e8-457a-97be-efe8e731619d">IProviderConverter Interface</a>
 

 

