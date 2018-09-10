---
UID: NN:casetup.ICertSrvSetup
title: ICertSrvSetup
author: windows-sdk-content
description: Defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a Certificate Services computer.
old-location: security\icertsrvsetup.htm
tech.root: seccrypto
ms.assetid: 6792a0d6-d304-481d-a97b-5fb7033c7eae
ms.author: windowssdkdev
ms.date: 08/29/2018
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
req.lib: 
req.dll: Certocm.dll
req.irql: 
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
req.typenames: 
req.redist: 
---

# ICertSrvSetup interface


## -description


The <b>ICertSrvSetup</b> interface defines functionality to install and uninstall Certification Authority (CA) and Certification Authority Web Enrollment roles on a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Services</a> computer.

Microsoft provides an implementation of this interface in the <b>CCertSrvSetup</b> class. For installation, you must call the <a href="https://msdn.microsoft.com/en-us/library/Bb736394(v=VS.85).aspx">InitializeDefaults</a> method before accessing any properties or calling any other methods on the <b>CCertSrvSetup</b> object.

In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_CCertSrvSetup</b> class identifier.

<b>Windows Server 2008 Standard:  </b>The following services are not available:<ul>
<li>Online Responder Service</li>
<li>Network Device Enrollment Service</li>
</ul>
In addition, the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) service has limited functionality:

<ul>
<li>V2 templates are not supported; therefore, autoenrollment is not supported.</li>
<li>Delegated enrollment agents are not supported.</li>
<li>Role separation is not supported.</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertSrvSetup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertSrvSetup</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb736386(v=VS.85).aspx">CAImportPFX</a>
</td>
<td align="left" width="63%">
Imports a CA certificate and its associated <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> into the "LocalMachine" store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736387(v=VS.85).aspx">GetCASetupProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for a CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736388(v=VS.85).aspx">GetExistingCACertificates</a>
</td>
<td align="left" width="63%">
Gets the collection of <b>CCertSrvSetupKeyInformation</b>  objects that represent valid CA certificates currently installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736389(v=VS.85).aspx">GetHashAlgorithmList</a>
</td>
<td align="left" width="63%">
Gets the list of <a href="https://msdn.microsoft.com/en-us/library/ms721586(v=VS.85).aspx">hashing algorithms</a> supported by the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) for an asymmetric key signature algorithm.

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
<a href="https://msdn.microsoft.com/en-us/library/Bb736394(v=VS.85).aspx">InitializeDefaults</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb736396(v=VS.85).aspx">IsPropertyEditable</a>
</td>
<td align="left" width="63%">
Indicates to the caller whether a specified property can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736397(v=VS.85).aspx">PostUnInstall</a>
</td>
<td align="left" width="63%">
This method is not implemented and is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736398(v=VS.85).aspx">PreUnInstall</a>
</td>
<td align="left" width="63%">
Temporarily saves role-specific state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736399(v=VS.85).aspx">SetCADistinguishedName</a>
</td>
<td align="left" width="63%">
Sets a CA common name and an optional distinguished name suffix.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736400(v=VS.85).aspx">SetCASetupProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for a CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736401(v=VS.85).aspx">SetDatabaseInformation</a>
</td>
<td align="left" width="63%">
Sets the database related information for the CA role.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736402(v=VS.85).aspx">SetParentCAInformation</a>
</td>
<td align="left" width="63%">
Sets the parent CA information for a subordinate CA configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb736403(v=VS.85).aspx">SetWebCAInformation</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Bb736384(v=VS.85).aspx">CAErrorId</a>


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

<a href="https://msdn.microsoft.com/en-us/library/Bb736385(v=VS.85).aspx">CAErrorString</a>


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




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

