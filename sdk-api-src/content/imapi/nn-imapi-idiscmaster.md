---
UID: NN:imapi.IDiscMaster
title: IDiscMaster
author: windows-driver-content
description: The IDiscMaster interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc.
old-location: imapi\idiscmaster.htm
old-project: imapi
ms.assetid: 1473e79e-a13a-4bc5-b80d-d8921fdc9952
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IDiscMaster, IDiscMaster interface [IMAPI], IDiscMaster interface [IMAPI],described, _win32_idiscmaster, base.idiscmaster, imapi.idiscmaster, imapi/IDiscMaster
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IDiscMaster
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMaster interface


## -description


The 
<b>IDiscMaster</b> interface allows an application to reserve an image mastering API, enumerate disc mastering formats and disc recorders supported by an image mastering object, and start a simulated or actual burn of a disc. Although an image mastering object can support several formats, it may not be possible to access all formats through a specific recorder. For this reason, you must select a recorder with 
<a href="https://msdn.microsoft.com/5f2e9135-d251-4702-b5d1-51d9b445a4f5">SetActiveDiscRecorder</a> after selecting a format with 
<a href="https://msdn.microsoft.com/fcc2840b-d302-4cd6-b576-1826c83b711e">SetActiveDiscMasterFormat</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscMaster</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiscMaster</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscMaster</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3c0d850-914b-47ae-b614-a292411e6832">ClearFormatContent</a>
</td>
<td align="left" width="63%">
Clears the contents of an unburned image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7190dbf6-6458-4228-a892-428183ea2742">EnumDiscMasterFormats</a>
</td>
<td align="left" width="63%">
Retrieves a format enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03daab81-11cf-4100-ab5e-3442a5972912">EnumDiscRecorders</a>
</td>
<td align="left" width="63%">
Retrieves a recorder enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37677090-fa1d-4515-9b01-13bfa55d8ebb">GetActiveDiscMasterFormat</a>
</td>
<td align="left" width="63%">
Retrieves the currently selected recorder format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdbc6108-c5c9-4083-84cd-7eae63d45c0f">GetActiveDiscRecorder</a>
</td>
<td align="left" width="63%">
Retrieves the active disc recorder format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens an IMAPI object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64966230-2042-46cb-9974-adbe382723a1">ProgressAdvise</a>
</td>
<td align="left" width="63%">
Registers for progress notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2729ff7-aefb-40cf-ae7b-9451fbe10bbb">ProgressUnadvise</a>
</td>
<td align="left" width="63%">
Cancels progress notifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a>
</td>
<td align="left" width="63%">
Burns the staged image to media in the active disc recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcc2840b-d302-4cd6-b576-1826c83b711e">SetActiveDiscMasterFormat</a>
</td>
<td align="left" width="63%">
Sets a new active recorder format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f2e9135-d251-4702-b5d1-51d9b445a4f5">SetActiveDiscRecorder</a>
</td>
<td align="left" width="63%">
Selects a new active disc recorder.

</td>
</tr>
</table> 

