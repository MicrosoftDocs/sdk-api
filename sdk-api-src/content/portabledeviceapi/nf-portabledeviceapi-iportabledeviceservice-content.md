---
UID: NF:portabledeviceapi.IPortableDeviceService.Content
title: IPortableDeviceService::Content
author: windows-sdk-content
description: Retrieves access to the service content.
old-location: wpdsdk\iportabledeviceservice_content.htm
old-project: wpd_sdk
ms.assetid: 36977b23-b03f-48bc-8313-ddfe2ef208de
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Content, Content method [Windows Portable Devices SDK], Content method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Content method, IPortableDeviceService.Content, IPortableDeviceService::Content, portabledeviceapi/IPortableDeviceService::Content, wpdsdk.iportabledeviceservice_content
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceService.Content
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceService::Content


## -description


The <b>Content</b> method retrieves access to the service content.


## -parameters




### -param ppContent [out]

The <a href="https://msdn.microsoft.com/73bf9a24-7fdc-4483-ad37-28d887d146d9">IPortableDeviceContent2</a> interface that accesses the service content.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> parameter was specified.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4af4201c-d3f6-4630-91ec-6509c51871a5">Enumerating Service Content</a>



<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>



<a href="https://msdn.microsoft.com/7fbd6f65-366a-49ea-a680-be77ca0d64f2">Retrieving Content-Object Properties</a>



<a href="https://msdn.microsoft.com/f762a571-83ea-4999-ad49-a51044bc790d">Writing Content-Object Properties</a>
 

 

