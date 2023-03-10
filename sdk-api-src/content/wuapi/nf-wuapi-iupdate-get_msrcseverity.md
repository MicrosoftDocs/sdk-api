---
UID: NF:wuapi.IUpdate.get_MsrcSeverity
title: IUpdate::get_MsrcSeverity (wuapi.h)
description: Gets the Microsoft Security Response Center severity rating of the update.
helpviewer_keywords: ["IUpdate interface [Windows Update Agent]","MsrcSeverity property","IUpdate.MsrcSeverity","IUpdate.get_MsrcSeverity","IUpdate::MsrcSeverity","IUpdate::get_MsrcSeverity","MsrcSeverity property [Windows Update Agent]","MsrcSeverity property [Windows Update Agent]","IUpdate interface","get_MsrcSeverity","wua.iupdate_msrcseverity","wuapi/IUpdate::MsrcSeverity","wuapi/IUpdate::get_MsrcSeverity"]
old-location: wua\iupdate_msrcseverity.htm
tech.root: wua
ms.assetid: ed3187c5-e175-4287-b930-2c283c9e93f3
ms.date: 12/05/2018
ms.keywords: IUpdate interface [Windows Update Agent],MsrcSeverity property, IUpdate.MsrcSeverity, IUpdate.get_MsrcSeverity, IUpdate::MsrcSeverity, IUpdate::get_MsrcSeverity, MsrcSeverity property [Windows Update Agent], MsrcSeverity property [Windows Update Agent],IUpdate interface, get_MsrcSeverity, wua.iupdate_msrcseverity, wuapi/IUpdate::MsrcSeverity, wuapi/IUpdate::get_MsrcSeverity
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_MsrcSeverity
 - wuapi/IUpdate::get_MsrcSeverity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.MsrcSeverity
 - IUpdate.get_MsrcSeverity
---

# IUpdate::get_MsrcSeverity


## -description

Gets the Microsoft Security Response Center severity rating of the update.

This property is read-only.

## -parameters

## -remarks

The following ratings are the possible severity ratings of a security issue that is fixed by an update. These ratings were revised by the Microsoft Security Response Center in November 2002.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="Critical"></a><a id="critical"></a><a id="CRITICAL"></a>Critical

</td>
<td width="60%">
A security issue whose exploitation could allow the propagation of an Internet worm without user action.

</td>
</tr>
<tr>
<td width="40%">
<a id="Important"></a><a id="important"></a><a id="IMPORTANT"></a>Important

</td>
<td width="60%">
A security issue whose exploitation could result in compromise of the confidentiality, integrity, or availability of users' data, or of the integrity or availability of processing resources.

</td>
</tr>
<tr>
<td width="40%">
<a id="Moderate"></a><a id="moderate"></a><a id="MODERATE"></a>Moderate

</td>
<td width="60%">
Exploitation is mitigated to a significant degree by factors such as default configuration, auditing, or difficulty of exploitation.

</td>
</tr>
<tr>
<td width="40%">
<a id="Low"></a><a id="low"></a><a id="LOW"></a>Low

</td>
<td width="60%">
A security issue whose exploitation is extremely difficult, or whose impact is minimal.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>