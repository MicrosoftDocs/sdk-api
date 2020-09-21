---
UID: NS:ndattrib.tagRootCauseInfo
title: RootCauseInfo (ndattrib.h)
description: Contains detailed information about the root cause of an incident.
helpviewer_keywords: ["*PRootCauseInfo","RCF_ISCONFIRMED","RCF_ISLEAF","RCF_ISTHIRDPARTY","RootCauseInfo","RootCauseInfo structure [NDF]","ndattrib/RootCauseInfo","ndf.rootcauseinfo"]
old-location: ndf\rootcauseinfo.htm
tech.root: NDF
ms.assetid: 01d02658-ae12-4465-94fc-7a966dcdd8fb
ms.date: 12/05/2018
ms.keywords: '*PRootCauseInfo, RCF_ISCONFIRMED, RCF_ISLEAF, RCF_ISTHIRDPARTY, RootCauseInfo, RootCauseInfo structure [NDF], ndattrib/RootCauseInfo, ndf.rootcauseinfo'
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ndattrib.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RootCauseInfo, *PRootCauseInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRootCauseInfo
 - ndattrib/tagRootCauseInfo
 - PRootCauseInfo
 - ndattrib/PRootCauseInfo
 - RootCauseInfo
 - ndattrib/RootCauseInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - RootCauseInfo
---

# RootCauseInfo structure


## -description

Contains detailed information about the root cause of an incident.

## -struct-fields

### -field pwszDescription

Type: <b>LPWSTR</b>

A string that describes the problem that caused the incident.

### -field rootCauseID

Type: <b>GUID</b>

The GUID that corresponds to the problem identified.

### -field rootCauseFlags

Type: <b>DWORD</b>

A numeric value that provides more information about the problem.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RCF_ISLEAF"></a><a id="rcf_isleaf"></a><dl>
<dt><b>RCF_ISLEAF</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The root cause corresponds to a leaf in the diagnostics tree. Root causes that are leafs are more likely to be closer to the problem that the user is trying to diagnose. 

</td>
</tr>
<tr>
<td width="40%"><a id="RCF_ISCONFIRMED"></a><a id="rcf_isconfirmed"></a><dl>
<dt><b>RCF_ISCONFIRMED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The root cause corresponds to a node with a <a href="/windows/desktop/api/ndhelper/ne-ndhelper-diagnosis_status">DIAGNOSIS_STATUS</a> value of <b>DS_CONFIRMED</b>. Problems with confirmed low health are more likely to correspond to the problem the user is trying to diagnose. 

</td>
</tr>
<tr>
<td width="40%"><a id="RCF_ISTHIRDPARTY"></a><a id="rcf_isthirdparty"></a><dl>
<dt><b>RCF_ISTHIRDPARTY</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The root cause comes from a third-party helper class extension rather than a native Windows helper class.

</td>
</tr>
</table>

### -field networkInterfaceID

Type: <b>GUID</b>

GUID of the network interface on which the problem occurred. If the problem is not interface-specific, this value is zero (0).

### -field pRepairs

Type: <b><a href="/windows/desktop/api/ndattrib/ns-ndattrib-repairinfoex">RepairInfoEx</a>*</b>

The repairs that are available to try and fix the problem.

### -field repairCount

Type: <b>USHORT</b>

The number of repairs available.

## -see-also

<a href="/windows/desktop/NDF/copyrootcauseinfo">CopyRootCauseInfo</a>



<a href="/windows/desktop/api/ndhelper/ne-ndhelper-diagnosis_status">DIAGNOSIS_STATUS</a>



<a href="/windows/desktop/NDF/freerootcauseinfos">FreeRootCauseInfos</a>



<a href="/windows/desktop/api/ndattrib/ns-ndattrib-repairinfoex">RepairInfoEx</a>