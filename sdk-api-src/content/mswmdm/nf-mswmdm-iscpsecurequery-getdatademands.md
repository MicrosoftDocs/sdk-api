---
UID: NF:mswmdm.ISCPSecureQuery.GetDataDemands
title: ISCPSecureQuery::GetDataDemands
author: windows-sdk-content
description: The GetDataDemands method reports which data the secure content provider needs to determine the rights and responsibility for a specified piece of content.
old-location: wmdm\iscpsecurequery_getdatademands.htm
tech.root: WMDM
ms.assetid: c4ed4da1-9378-4c35-8f03-b028e37c1707
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDataDemands, GetDataDemands method [windows Media Device Manager], GetDataDemands method [windows Media Device Manager],ISCPSecureQuery interface, ISCPSecureQuery interface [windows Media Device Manager],GetDataDemands method, ISCPSecureQuery.GetDataDemands, ISCPSecureQuery::GetDataDemands, ISCPSecureQueryGetDataDemands, mswmdm/ISCPSecureQuery::GetDataDemands, wmdm.iscpsecurequery_getdatademands
ms.topic: method
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - ISCPSecureQuery.GetDataDemands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISCPSecureQuery::GetDataDemands


## -description



The <b>GetDataDemands</b> method reports which data the secure content provider needs to determine the rights and responsibility for a specified piece of content.




## -parameters




### -param pfuFlags [out]

Flags describing the data required by the secure content provider to make decisions. This parameter is included in the output message authentication code. At least one of the following flags must be used.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_SCP_RIGHTS_DATA</td>
<td>The secure content provider needs data to determine rights for the content.</td>
</tr>
<tr>
<td>WMDM_SCP_EXAMINE_DATA</td>
<td>The secure content provider needs data to determine whether it is responsible for the content.</td>
</tr>
<tr>
<td>WMDM_SCP_DECIDE_DATA</td>
<td>The secure content provider needs data to determine whether to allow the content to be downloaded.</td>
</tr>
<tr>
<td>WMDM_SCP_EXAMINE_EXTENSION</td>
<td>The secure content provider needs to examine the file name extension to determine whether to allow the content to be downloaded.</td>
</tr>
<tr>
<td>WMDM_SCP_PROTECTED_OUTPUT</td>
<td>The secure content provider needs protected output.</td>
</tr>
<tr>
<td>WMDM_SCP_UNPROTECTED_OUTPUT</td>
<td>The secure content provider needs unprotected output.</td>
</tr>
</table>
 


### -param pdwMinRightsData [out]

Pointer to a <b>DWORD</b> specifying the minimum amount of data needed to determine rights for this content. This parameter is included in the output message authentication code.


### -param pdwMinExamineData [out]

Pointer to a <b>DWORD</b> containing the minimum number of bytes of data that the secure content provider needs to determine whether it is responsible for the content. This parameter is included in the output message authentication code.


### -param pdwMinDecideData [out]

Pointer to a <b>DWORD</b> containing the minimum number of bytes of data that the secure content provider needs to determine whether to allow the content to be downloaded. This parameter is included in the output message authentication code.


### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MAC_CHECK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The message authentication code is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is an invalid or <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



This method must be called before any of the other methods of <b>ISCPSecureQuery</b> are called.

This method is called after any certificate exchanges have been successfully finished. The secure content provider fills in the parameters with the flags and data that describe its requirements for making decisions about the content.

If the secure content provider sets the WMDM_SCP_RIGHTS_DATA flag, then Windows Media Device Manager sends the amount of data specified in <i>pdwMinRightsData</i> by calling <a href="https://msdn.microsoft.com/3d9991f4-ce20-45c4-a408-d7a846b019ef">ISCPSecureQuery::GetRights</a>.

If the secure content provider sets the WMDM_SCP_EXAMINE_DATA flag, then Windows Media Device Manager sends the amount of data specified in <i>pdwMinExamineData</i> by calling <a href="https://msdn.microsoft.com/e12d8b55-5600-4178-8b2b-8afe8ade6818">ISCPSecureQuery::ExamineData</a>.

If the secure content provider sets the WMDM_SCP_DECIDE_DATA flag, then Windows Media Device Manager sends the amount of data specified in <i>pdwMinDecideData</i> by calling <a href="https://msdn.microsoft.com/cbcc8999-d7e4-4b67-a5ba-dd850ff7a07a">ISCPSecureQuery::MakeDecision</a>.

If no examine flags are set, Windows Media Device Manager does not make any more calls. If no decide flags are set, Windows Media Device Manager still calls <a href="https://msdn.microsoft.com/e12d8b55-5600-4178-8b2b-8afe8ade6818">ISCPSecureQuery::ExamineData</a>.

If this method does not return S_OK, then Windows Media Device Manager does not make any further calls to this secure content provider.




## -see-also




<a href="https://msdn.microsoft.com/d5f96629-26a1-4e83-a6a8-2d60c463f407">ISCPSecureQuery Interface</a>
 

 

