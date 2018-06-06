---
UID: NN:casetup.ICertSrvSetup
title: ICertSrvSetup
author: windows-sdk-content
description: Defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a Certificate Services computer.
old-location: security\icertsrvsetup.htm
old-project: SecCrypto
ms.assetid: 6792a0d6-d304-481d-a97b-5fb7033c7eae
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: ICertSrvSetup, ICertSrvSetup interface [Security], ICertSrvSetup interface [Security],described, casetup/ICertSrvSetup, security.icertsrvsetup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CEPSetupProperty
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup
product: Windows
targetos: Windows
req.lib: 
req.dll: Certocm.dll
req.irql: 
---

# ICertSrvSetup interface


## -description


The <b>ICertSrvSetup</b> interface defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Services</a> computer.

Microsoft provides an implementation of this interface in the <b>CCertSrvSetup</b> class. For installation, you must call the <a href="https://msdn.microsoft.com/dff7e2e2-291a-4ea9-858a-8d98d96f79ac">InitializeDefaults</a> method before accessing any properties or calling any other methods on the <b>CCertSrvSetup</b> object.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CCertSrvSetup</b> class identifier.

<b>Windows Server 2008 Standard:  </b>The following services are not available:<ul>
<li>Online Responder Service</li>
<li>Network Device Enrollment Service</li>
</ul>
In addition, the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) service has limited functionality:

<ul>
<li>V2 templates are not supported; therefore, autoenrollment is not supported.</li>
<li>Delegated enrollment agents are not supported.</li>
<li>Role separation is not supported.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetup</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertSrvSetup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertSrvSetup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a661b74b-04ba-49b9-bde2-3e368ae6228e">CAImportPFX</a>
</td>
<td align="left" width="63%">
Imports a CA certificate and its associated <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> into the "LocalMachine" store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7da5f111-206d-40e1-9c40-4782118c3d49">GetCASetupProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for a CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd8c7bac-b6db-41f2-a648-e01ebd09c41c">GetExistingCACertificates</a>
</td>
<td align="left" width="63%">
Gets the collection of <b>CCertSrvSetupKeyInformation</b>  objects that represent valid CA certificates currently installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/451c240d-8df9-4f4a-ab0e-56c5252d3b50">GetHashAlgorithmList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hashing algorithms</a> supported by the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) for an asymmetric key signature algorithm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9360522a-05fd-41ae-95b1-9270a9f4f728">GetKeyLengthList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key lengths</a> supported by the specified CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a57590d3-0882-4407-b920-964c0e489f80">GetPrivateKeyContainerList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> names stored by the specified CSP for asymmetric key signature algorithms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0915981-8023-4ce8-a870-7acc75c574ac">GetProviderNameList</a>
</td>
<td align="left" width="63%">
Gets the list of CSPs that provide asymmetric key signature algorithms on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/404e5c34-f614-4555-9062-c28d4aac5c4b">GetSupportedCATypes</a>
</td>
<td align="left" width="63%">
Gets the types of CAs that can be installed on a computer under the caller context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dff7e2e2-291a-4ea9-858a-8d98d96f79ac">InitializeDefaults</a>
</td>
<td align="left" width="63%">
Initializes a <b>CCertSrvSetup</b> object with default values to enable installation of a CA role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e07b1cdd-ccb6-4398-862b-521ac1d39f66">Install</a>
</td>
<td align="left" width="63%">
Installs a CA role as configured in the <b>CCertSrvSetup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2facae59-aa96-4ac7-97e1-ff094022681a">IsPropertyEditable</a>
</td>
<td align="left" width="63%">
Indicates to the caller whether a specified property can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5ec32ec-616c-4460-bd1c-6e70c61b5234">PostUnInstall</a>
</td>
<td align="left" width="63%">
This method is not implemented and is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2872a7fb-fe96-4ace-b5f4-af88350835ab">PreUnInstall</a>
</td>
<td align="left" width="63%">
Temporarily saves role-specific state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d513d4fd-abc7-44e6-822e-955de8613d55">SetCADistinguishedName</a>
</td>
<td align="left" width="63%">
Sets a CA common name and an optional distinguished name suffix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91df1926-a4b6-4ba2-ab59-0258293fc1c0">SetCASetupProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for a CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae690d59-21fe-4429-8e80-ee2ce19a7090">SetDatabaseInformation</a>
</td>
<td align="left" width="63%">
Sets the database related information for the CA role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73c4782d-579d-48d7-b999-f15a2443bbca">SetParentCAInformation</a>
</td>
<td align="left" width="63%">
Sets the parent CA information for a subordinate CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c8d6b06-d36c-496f-8d5a-da20f09a2b0a">SetWebCAInformation</a>
</td>
<td align="left" width="63%">
Sets the CA information for the Certification Authority Web Enrollment role.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/462fb4a6-2aad-46d4-98e0-32c095eff5c7">CAErrorId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the ID for additional error information related to a failed CA specification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/154397f8-aa0e-4d74-b18e-b68b46fdfcdb">CAErrorString</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the string data for additional error information related to a failed CA specification.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

