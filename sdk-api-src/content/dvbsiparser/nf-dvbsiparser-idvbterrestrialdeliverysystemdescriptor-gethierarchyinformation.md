---
UID: NF:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor.GetHierarchyInformation
title: IDvbTerrestrialDeliverySystemDescriptor::GetHierarchyInformation
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbterrestrialdeliverysystemdescriptor_gethierarchyinformation.htm
old-project: mstv
ms.assetid: 8ad35924-b6e0-47b1-9873-14bf48574669
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetHierarchyInformation, GetHierarchyInformation method [Microsoft TV Technologies], GetHierarchyInformation method [Microsoft TV Technologies],IDvbTerrestrialDeliverySystemDescriptor interface, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetHierarchyInformation method, IDvbTerrestrialDeliverySystemDescriptor.GetHierarchyInformation, IDvbTerrestrialDeliverySystemDescriptor::GetHierarchyInformation, IDvbTerrestrialDeliverySystemDescriptorGetHierarchyInformation, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetHierarchyInformation, mstv.idvbterrestrialdeliverysystemdescriptor_gethierarchyinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbTerrestrialDeliverySystemDescriptor.GetHierarchyInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTerrestrialDeliverySystemDescriptor::GetHierarchyInformation


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetHierarchyInformation</b> method returns the hierarchy alpha information.


## -parameters




### -param pbVal [out]

Receives the hierarchy_information field.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7000f937-2f58-43c1-b0e1-60d3171485b0">IDvbTerrestrialDeliverySystemDescriptor Interface</a>
 

 

