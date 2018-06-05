---
UID: NF:wpcapi.IWPCProviderSupport.GetCurrent
title: IWPCProviderSupport::GetCurrent
author: windows-sdk-content
description: Retrieves the GUID of the current provider.
old-location: parcon\iwpcprovidersupport_getcurrent.htm
old-project: parcon
ms.assetid: 36496cba-229c-45bb-9608-04fb4b1955ae
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetCurrent, GetCurrent method, GetCurrent method,IWPCProviderSupport interface, IWPCProviderSupport interface,GetCurrent method, IWPCProviderSupport.GetCurrent, IWPCProviderSupport::GetCurrent, parcon.iwpcprovidersupport_getcurrent, wpcapi/IWPCProviderSupport::GetCurrent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wpcapi.h
api_name:
-	IWPCProviderSupport.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWPCProviderSupport::GetCurrent


## -description


Retrieves the GUID of the current provider.


## -parameters




### -param pguidProvider [out]

The GUID of the current provider.


## -returns



If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pguidProvider</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



The <i>pguidProvider</i> parameter will be a null GUID if there is no currently selected provider.




## -see-also




<a href="https://msdn.microsoft.com/5c2a793b-d136-4d03-9e46-b24009af2c7d">IWPCProviderSupport</a>
 

 

