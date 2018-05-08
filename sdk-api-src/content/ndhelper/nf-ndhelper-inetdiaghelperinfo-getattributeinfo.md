---
UID: NF:ndhelper.INetDiagHelperInfo.GetAttributeInfo
title: INetDiagHelperInfo::GetAttributeInfo
author: windows-driver-content
description: The GetAttributeInfo method retrieves the list of key parameters needed by the Helper Class Extension.
old-location: ndf\inetdiaghelperinfo_getattributeinfo.htm
old-project: NDF
ms.assetid: 0c1a12f3-357f-4d96-b0ef-99d788b6e020
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetAttributeInfo, GetAttributeInfo method [NDF], GetAttributeInfo method [NDF],INetDiagHelperInfo interface, INetDiagHelperInfo interface [NDF],GetAttributeInfo method, INetDiagHelperInfo.GetAttributeInfo, INetDiagHelperInfo::GetAttributeInfo, ndf.inetdiaghelperinfo_getattributeinfo, ndhelper/INetDiagHelperInfo::GetAttributeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REPAIR_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ndhelper.h
api_name:
-	INetDiagHelperInfo.GetAttributeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetDiagHelperInfo::GetAttributeInfo


## -description


The <b>GetAttributeInfo</b> method retrieves the list of key parameters needed by the Helper Class Extension.


## -parameters




### -param pcelt [out]

A pointer to a count of elements in the array pointed to by <i>pprgAttributeInfos</i>.


### -param pprgAttributeInfos [out]

A pointer to an array of <a href="https://msdn.microsoft.com/a4de3031-7199-4537-a97e-f33059383d6b">HelperAttributeInfo</a> structures that contain helper class key parameters.


## -returns



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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to perform the diagnosis or repair operation.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the diagnoses or repairs.




## -remarks



The key parameter list is used by NDF to determine whether enough information is available for the extension to perform diagnosis.  If the hypothesis to call the extension lacks a key attribute, the extension will not be called.  Optional attributes will not be returned by this call.




## -see-also




<a href="https://msdn.microsoft.com/815e2338-0055-4078-a9a5-197db449c33d">INetDiagHelperInfo</a>
 

 

