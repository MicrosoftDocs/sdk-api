---
UID: NF:wmnetsourcecreator.INSNetSourceCreator.GetNetSourceAdminInterface
title: INSNetSourceCreator::GetNetSourceAdminInterface
author: windows-sdk-content
description: The GetNetSourceAdminInterface method retrieves a pointer to the IDispatch interface of the administrative network source object.
old-location: wmformat\insnetsourcecreator_getnetsourceadmininterface.htm
old-project: wmformat
ms.assetid: 147b431f-84ed-40b9-85a8-3c220b56cd3f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetNetSourceAdminInterface, GetNetSourceAdminInterface method [windows Media Format], GetNetSourceAdminInterface method [windows Media Format],INSNetSourceCreator interface, INSNetSourceCreator interface [windows Media Format],GetNetSourceAdminInterface method, INSNetSourceCreator.GetNetSourceAdminInterface, INSNetSourceCreator::GetNetSourceAdminInterface, INSNetSourceCreatorGetNetSourceAdminInterface, wmformat.insnetsourcecreator_getnetsourceadmininterface, wmnetsourcecreator/INSNetSourceCreator::GetNetSourceAdminInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmnetsourcecreator.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WindowsMediaLibrarySharingDeviceAuthorizationStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	INSNetSourceCreator.GetNetSourceAdminInterface
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# INSNetSourceCreator::GetNetSourceAdminInterface


## -description



The <b>GetNetSourceAdminInterface</b> method retrieves a pointer to the <b>IDispatch</b> interface of the administrative network source object.




## -parameters




### -param pszStreamName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the desired network protocol. Typically, this value is either "http\0" or "mms\0".


### -param pVal [out]

Pointer to a <b>VARIANT</b> that receives the address of the <b>IDispatch</b> interface on successful return. Use this interface pointer to obtain the interface pointer of the desired network admin interface: <a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource</a>, <a href="https://msdn.microsoft.com/6d334725-11d5-4249-a83d-fc8c1c35a56f">IWMSInternalAdminNetSource2</a>, or <a href="https://msdn.microsoft.com/b4ca08a4-6e2d-4646-b101-67bac67300b1">IWMSInternalAdminNetSource3</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both of the parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory for an internal resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_UNKNOWN_PROTOCOL</b></dt>
</dl>
</td>
<td width="60%">
The protocol specified by <i>pwszStreamName</i> is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/39e692a6-fb68-447f-bd28-8d216776157a">INSNetSourceCreator Interface</a>
 

 

