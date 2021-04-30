---
UID: NF:winsync.ISyncKnowledge2.GetMinimumSupportedVersion
title: ISyncKnowledge2::GetMinimumSupportedVersion (winsync.h)
description: Gets the minimum supported version of Microsoft Sync Framework components that can be used with this object.
helpviewer_keywords: ["GetMinimumSupportedVersion","GetMinimumSupportedVersion method [Windows Sync]","GetMinimumSupportedVersion method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","GetMinimumSupportedVersion method","ISyncKnowledge2.GetMinimumSupportedVersion","ISyncKnowledge2::GetMinimumSupportedVersion","winsync.isyncknowledge2_getminimumsupportedversion","winsync/ISyncKnowledge2::GetMinimumSupportedVersion"]
old-location: winsync\isyncknowledge2_getminimumsupportedversion.htm
tech.root: winsync
ms.assetid: 06b5794e-ba46-499f-b85c-f0acb4fd79a7
ms.date: 12/05/2018
ms.keywords: GetMinimumSupportedVersion, GetMinimumSupportedVersion method [Windows Sync], GetMinimumSupportedVersion method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetMinimumSupportedVersion method, ISyncKnowledge2.GetMinimumSupportedVersion, ISyncKnowledge2::GetMinimumSupportedVersion, winsync.isyncknowledge2_getminimumsupportedversion, winsync/ISyncKnowledge2::GetMinimumSupportedVersion
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncKnowledge2::GetMinimumSupportedVersion
 - winsync/ISyncKnowledge2::GetMinimumSupportedVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncKnowledge2.GetMinimumSupportedVersion
---

# ISyncKnowledge2::GetMinimumSupportedVersion


## -description

Gets the minimum supported version of <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a> components that can be used with this object.

## -parameters

### -param pVersion [out]

The minimum supported version of Microsoft Sync Framework components that can be used with this object.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This method is used only with synchronization sessions that use <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a> components.</div>
<div> </div>
A knowledge object that has a version of <b>SYNC_SERIALIZATION_VERSION_V2</b> supports components that are compatible with Sync Framework 1.0 when the knowledge object contains only elements that are compatible with Sync Framework 1.0. In this situation, <b>GetMinSupportedVersion</b> returns a version of <b>SYNC_SERIALIZATION_VERSION_V1</b>.

For an overview of what is involved in building synchronization providers using  <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a>, see <a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>



<a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_full_enumeration_action">SYNC_SERIALIZATION_VERSION Enumeration</a>