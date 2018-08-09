---
UID: NF:mswmdm.IMDSPDevice2.GetCanonicalName
title: IMDSPDevice2::GetCanonicalName
author: windows-sdk-content
description: The GetCanonicalPName method gets the canonical name of a device.
old-location: wmdm\imdspdevice2_getcanonicalname.htm
old-project: WMDM
ms.assetid: 0888c780-e358-45ae-809b-34a19d496059
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCanonicalName, GetCanonicalName method [windows Media Device Manager], GetCanonicalName method [windows Media Device Manager],IMDSPDevice2 interface, IMDSPDevice2 interface [windows Media Device Manager],GetCanonicalName method, IMDSPDevice2.GetCanonicalName, IMDSPDevice2::GetCanonicalName, IMDSPDevice2GetPnPName, mswmdm/IMDSPDevice2::GetCanonicalName, wmdm.imdspdevice2_getcanonicalname
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDevice2.GetCanonicalName
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice2::GetCanonicalName


## -description



The <b>GetCanonicalPName</b> method gets the canonical name of a device.




## -parameters




### -param pwszPnPName [out]

A wide character, null-terminated buffer holding the canonical name. The caller allocates and releases this buffer.


### -param nMaxChars [in]

Integer containing the maximum number of characters that can be placed in <i>pwszCanonicalName</i>, including the termination character.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.




## -remarks



This method returns a canonical name for the device. The service provider should return the device path name of the device as its canonical name. The service provider is passed the device path name in the <b>CreateDevice</b> method on the <a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2</a> interface.

This is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>



<a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2 Interface</a>



<a href="https://msdn.microsoft.com/f724ef14-c572-41ca-a56b-fde85d7620e0">IMDServiceProvider2::CreateDevice</a>
 

 

