---
UID: NF:wmsdkidl.WMCreateLicenseRevocationAgent
title: WMCreateLicenseRevocationAgent function (wmsdkidl.h)
author: windows-sdk-content
description: The WMCreateLicenseRevocationAgent function creates a license revocation object.
old-location: wmformat\wmcreatelicenserevocationagent.htm
tech.root: wmformat
ms.assetid: 46898846-780f-4a86-93c7-826f55c358ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WMCreateLicenseRevocationAgent, WMCreateLicenseRevocationAgent function [windows Media Format], wmformat.wmcreatelicenserevocationagent, wmsdkidl/WMCreateLicenseRevocationAgent
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateLicenseRevocationAgent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WMCreateLicenseRevocationAgent function


## -description



The <b>WMCreateLicenseRevocationAgent</b> function creates a license revocation object.




## -parameters




### -param pCallback [in]

Address of the <b>IUnknown</b> interface of the object that implements the <a href="https://msdn.microsoft.com/en-us/library/Dd798545(v=VS.85).aspx">IWMStatusCallback::OnStatus</a> callback method used to communicate license revocation status to the application.


### -param ppLicenseRevocationAgent [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd757225(v=VS.85).aspx">IWMLicenseRevocationAgent</a> interface of the newly created license revocation agent object.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The function succeeded.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>The function is unable to allocate memory for the new object.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/10fa8f96-8030-4727-af5d-7c06229d05d8">Functions</a>
 

 

