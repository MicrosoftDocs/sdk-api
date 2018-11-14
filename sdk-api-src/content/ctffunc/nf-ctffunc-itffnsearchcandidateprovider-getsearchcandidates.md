---
UID: NF:ctffunc.ITfFnSearchCandidateProvider.GetSearchCandidates
title: ITfFnSearchCandidateProvider::GetSearchCandidates
author: windows-sdk-content
description: Gets a list of conversion candidates for a given string without generating any IME-related messages or events.
old-location: tsf\itffnsearchcandidateprovider_getsearchcandidates.htm
tech.root: TSF
ms.assetid: 7D7E8171-229F-4D9C-B086-D68E064A8A4C
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetSearchCandidates, GetSearchCandidates method [Text Services Framework], GetSearchCandidates method [Text Services Framework],ITfFnSearchCandidateProvider interface, ITfFnSearchCandidateProvider interface [Text Services Framework],GetSearchCandidates method, ITfFnSearchCandidateProvider.GetSearchCandidates, ITfFnSearchCandidateProvider::GetSearchCandidates, ctffunc/ITfFnSearchCandidateProvider::GetSearchCandidates, tsf.itffnsearchcandidateprovider_getsearchcandidates
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - Ctffunc.h
api_name:
 - ITfFnSearchCandidateProvider.GetSearchCandidates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- ctffunc.h
: 
- ITfFnSearchCandidateProvider.GetSearchCandidates
: 
---

# ITfFnSearchCandidateProvider::GetSearchCandidates


## -description


Gets a list of conversion candidates for a given string without generating any IME-related messages or events.


## -parameters




### -param bstrQuery [in]

A string that specifies the reading string that the text service attempts to convert.


### -param bstrApplicationId [in]

App-specified string that enables a text service to optionally provide different candidates to different apps or contexts based on input history. You can pass an empty <b>BSTR</b>, L””, for a generic context.


### -param pplist [out]

An <a href="https://msdn.microsoft.com/e41ba461-6337-4feb-ba16-3942920ebb9f">ITfCandidateList</a> that receives the requested candidate data.


## -returns



This method can return one of these values.

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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No candidates could be returned for the input string, <i>pplist</i> may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5DD99E0A-42A2-4EA5-B24F-5C439F5D7EEF">ITfFnSearchCandidateProvider</a>



<a href="https://msdn.microsoft.com/7cb7c94c-1526-48e1-9ab0-068e03a462c7">SearchPaneQueryLinguisticDetails</a>



<a href="https://msdn.microsoft.com/dcc172f9-4fc3-46f4-a1db-0e75fceafb28">SetResult</a>
 

 

