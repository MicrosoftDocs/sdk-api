---
UID: NN:comsvcs.ICrmFormatLogRecords
title: ICrmFormatLogRecords
author: windows-sdk-content
description: Converts the log records to viewable format so that they can be presented using a generic monitoring tool.
old-location: cos\icrmformatlogrecords.htm
tech.root: cossdk
ms.assetid: aa801bd0-5253-4f9f-8859-b808d4dc081b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICrmFormatLogRecords, ICrmFormatLogRecords interface [COM+], ICrmFormatLogRecords interface [COM+],described, _dtc_ICrmFormatLogRecords_Interface, comsvcs/ICrmFormatLogRecords, cos.icrmformatlogrecords
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmFormatLogRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmFormatLogRecords interface


## -description


Converts the log records to viewable format so that they can be presented using a generic monitoring tool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmFormatLogRecords</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICrmFormatLogRecords</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ICrmFormatLogRecords</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681297(v=VS.85).aspx">GetColumn</a>
</td>
<td align="left" width="63%">
Formats one unstructured log record into an array of viewable fields.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686549(v=VS.85).aspx">GetColumnCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of fields (columns) in a log record of the type used by this CRM Compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686067(v=VS.85).aspx">GetColumnHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the names of the fields (columns).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms688148(v=VS.85).aspx">GetColumnVariants</a>
</td>
<td align="left" width="63%">
Formats one structured log record into an array of viewable fields.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680326(v=VS.85).aspx">COM+ Compensating Resource Manager</a>
 

 

