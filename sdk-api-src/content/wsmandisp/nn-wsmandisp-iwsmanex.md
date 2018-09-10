---
UID: NN:wsmandisp.IWSManEx
title: IWSManEx
author: windows-sdk-content
description: Extends the methods and properties of the IWSMan interface to include creating IWSManResourceLocator objects, methods that return enumeration and session flag values, and a method to get extended error information.
old-location: winrm\iwsmanex.htm
tech.root: WinRM
ms.assetid: 23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSManEx, IWSManEx interface [Windows Remote Management], IWSManEx interface [Windows Remote Management],described, winrm.iwsmanex, wsmandisp/ IWSManEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSManEx interface


## -description


Extends the methods and properties of the <a href="https://msdn.microsoft.com/4e5acfa6-9883-4716-ac69-92161c926c66">IWSMan</a> 
    interface to include creating 
    <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> objects, methods that return 
    enumeration and session flag values, and a method to get extended error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n"> IWSManEx</b> interface inherits from <a href="https://msdn.microsoft.com/4e5acfa6-9883-4716-ac69-92161c926c66">IWSMan</a>. <b> IWSManEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b> IWSManEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">CreateResourceLocator</a>
</td>
<td align="left" width="63%">
Creates a new instance of an 
     <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9af95ac-4543-4d8b-ac6e-15e89b73713e">IWSManEx.SessionFlagCredUsernamePassword</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagCredUsernamePassword</b> for use 
     in the <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8fe2077-0606-4517-8e50-dc42a4c39b77">IWSManEx.SessionFlagEnableSPNServerPort</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagEnableSPNServerPort</b> for use 
     in the <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec96e873-ecb6-4d89-ada3-41c889544091">IWSManEx.SessionFlagNoEncryption</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagNoEncryption</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/683054fd-7ee3-4c90-a5cd-234e7d60349d">IWSManEx.SessionFlagSkipCACheck</a>
</td>
<td align="left" width="63%">
Returns the value of the  authentication flag <b>WSManFlagSkipCACheck</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf364e3a-e532-48cf-9b88-fdc661e70ffa">IWSManEx.SessionFlagSkipCNCheck</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagSkipCNCheck</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/0ccab9bf-f8b4-432e-92d1-b5a5d3a2dfe5">IWSMan::CreateSession</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b7457e2-1c19-4b33-bb38-5068f3c295cb">IWSManEx.SessionFlagUseBasic</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseBasic</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">IWSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3aa44847-932e-49c6-a7fd-966a2bb3539d">IWSManEx.SessionFlagUseDigest</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseDigest</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f9670a5-2bf3-4971-8f7e-8cc677acfb65">IWSManEx.SessionFlagUseNegotiate</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseNegotiate</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af3f7512-c1d5-4c4d-b79a-b0bf8b95be6d">IWSManEx.SessionFlagUseNoAuthentication</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseNoAuthentication</b> for use 
     in the <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99c96057-fbd7-4d8c-a204-1660f84d640f">IWSManEx.SessionFlagUTF8</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUTF8</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14b949d8-774b-4224-ab08-b52ff71ab1bb">IWSManEx.WSMan.SessionFlagUseKerberos</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseKerberos</b> for use in the 
     <i>flags</i> parameter of 
     <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a>. This method provides a more 
     efficient syntax for using the constant so that scripts are not required to set a constant value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1995b4bd-dc2f-4f43-8e08-52ea1899c2c5">IWSManEx::EnumerationFlagHierarchyDeep</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagHierarchyDeep</b> for use 
     in the <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72528ef3-3e38-4f1f-a686-45c3caa1d9d3">IWSManEx::EnumerationFlagHierarchyDeepBasePropsOnly</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant 
     <b>EnumerationFlagHierarchyDeepBasePropsOnly</b> for use in the 
     <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/590cf20d-56bc-4472-9d40-cc423bfb00df">IWSManEx::EnumerationFlagHierarchyShallow</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagHierarchyShallow</b> for 
     use in the <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f94dc9cc-a4c5-44b8-9ace-63b80b1087d2">IWSManEx::EnumerationFlagNonXmlText</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>WSManFlagNonXmlText</b> for use in the 
     <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f94dc9cc-a4c5-44b8-9ace-63b80b1087d2">IWSManEx::EnumerationFlagNonXmlText</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>WSManFlagNonXmlText</b> for use in the 
     <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8297f17-962d-4f52-909e-e26427af9ab2">IWSManEx::EnumerationFlagReturnEPR</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagReturnEPR</b> for use in 
     the <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19993342-a805-4d92-ac80-40f568b53800">IWSManEx::EnumerationFlagReturnObject</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagReturnObject</b> for use 
     in the <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ded5083-5f4a-4e07-96d6-7856c0a2f340">IWSManEx::EnumerationFlagReturnObjectAndEPR</a>
</td>
<td align="left" width="63%">
Returns the value of the enumeration constant <b>EnumerationFlagReturnObjectAndEPR</b> 
     for use in the <i>flags</i> parameter of the 
     <a href="https://msdn.microsoft.com/b1a4815e-93aa-4a30-a67e-c52fd06c1ee1">IWSManSession::Enumerate</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af5ae515-458a-4d7f-80f8-0fd51f97e7f1">IWSManEx::GetErrorMessage</a>
</td>
<td align="left" width="63%">
Returns a formatted string containing the text of an error number.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4e5acfa6-9883-4716-ac69-92161c926c66">IWSMan</a>



<a href="https://msdn.microsoft.com/45895a4e-b7de-4469-ae78-6d1d3f9d6145">WSMan</a>



<a href="https://msdn.microsoft.com/c996f074-f14b-4edd-80b7-8f4de4cbabb0">Windows Remote Management Reference</a>
 

 

