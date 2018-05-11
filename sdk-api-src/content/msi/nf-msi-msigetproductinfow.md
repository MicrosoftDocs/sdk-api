---
UID: NF:msi.MsiGetProductInfoW
title: MsiGetProductInfoW function
author: windows-driver-content
description: The MsiGetProductInfo function returns product information for published and installed products.
old-location: setup\msigetproductinfo.htm
old-project: Msi
ms.assetid: 336a68d6-5239-4313-b6c7-8091907a0e35
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: INSTALLPROPERTY_HELPLINK, INSTALLPROPERTY_HELPTELEPHONE, INSTALLPROPERTY_INSTALLDATE, INSTALLPROPERTY_INSTALLEDLANGUAGE, INSTALLPROPERTY_INSTALLEDPRODUCTNAME, INSTALLPROPERTY_INSTALLLOCATION, INSTALLPROPERTY_INSTALLSOURCE, INSTALLPROPERTY_LOCALPACKAGE, INSTALLPROPERTY_PUBLISHER, INSTALLPROPERTY_URLINFOABOUT, INSTALLPROPERTY_URLUPDATEINFO, INSTALLPROPERTY_VERSIONMAJOR, INSTALLPROPERTY_VERSIONMINOR, INSTALLPROPERTY_VERSIONSTRING, MsiGetProductInfo, MsiGetProductInfo function, MsiGetProductInfoA, MsiGetProductInfoW, _msi_msigetproductinfo, msi/MsiGetProductInfo, msi/MsiGetProductInfoA, msi/MsiGetProductInfoW, setup.msigetproductinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetProductInfoW (Unicode) and MsiGetProductInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_CLIENT_VERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
-	Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
-	MsiGetProductInfo
-	MsiGetProductInfoA
-	MsiGetProductInfoW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiGetProductInfoW function


## -description



			The 
<b>MsiGetProductInfo</b> function returns product information for published and installed products.


## -parameters




### -param szProduct [in]

Specifies the product code for the product.


### -param szAttribute

TBD


### -param lpValueBuf [out]

Pointer to a buffer that receives the property value. This parameter can be null.


### -param pcchValueBuf [in, out]

 Pointer to a variable that specifies the size, in characters, of the buffer pointed to by the <i>lpValueBuf</i> parameter. On input, this is the full size of the buffer, including a space for a terminating null character. If the buffer passed in is too small, the count returned does not include the terminating null character. 




If <i>lpValueBuf</i> is null, <i>pcchValueBuf</i> can be null. In this case, the function checks that the property is registered correctly with the product.


#### - szProperty [in]

Specifies the property to be retrieved.  

The 
<a href="https://msdn.microsoft.com/f63fc1e3-ac08-4c7b-8ce3-e02c59b716ab">Required Properties</a> are guaranteed to be available, but other properties are available only if that property is set. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>. The properties in the following list can be retrieved only from applications that are installed.

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_HELPLINK"></a><a id="installproperty_helplink"></a><dl>
<dt><b>INSTALLPROPERTY_HELPLINK</b></dt>
</dl>
</td>
<td width="60%">
Support link. For more information, see 
the <a href="https://msdn.microsoft.com/1f657f62-9e7d-466e-8f3e-084093c0e675">ARPHELPLINK</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_HELPTELEPHONE"></a><a id="installproperty_helptelephone"></a><dl>
<dt><b>INSTALLPROPERTY_HELPTELEPHONE</b></dt>
</dl>
</td>
<td width="60%">
Support telephone. For more information, see 
the <a href="https://msdn.microsoft.com/4547a419-3bcc-4274-9eb3-96c7987a4ebf">ARPHELPTELEPHONE</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLDATE"></a><a id="installproperty_installdate"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLDATE</b></dt>
</dl>
</td>
<td width="60%">
The last time this product received service. The value of this property is replaced each time a patch is applied or removed from the product or the /v <a href="https://msdn.microsoft.com/a70d8cc8-af47-4472-aabc-97481d97080d">Command-Line Option</a> is used to repair the product.  If the product has received no repairs or patches this property contains the time this product was installed on this computer.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLEDLANGUAGE"></a><a id="installproperty_installedlanguage"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLEDLANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Installed language.


<b><a href="https://msdn.microsoft.com/89662e62-53fb-4b50-8583-80518c6fda6d">Windows Installer 4.5 and earlier</a>:  </b>Not supported.



</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></a><a id="installproperty_installedproductname"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLEDPRODUCTNAME</b></dt>
</dl>
</td>
<td width="60%">
Installed product name. For more information, see 
the <a href="https://msdn.microsoft.com/0a9f5be1-9da2-47a7-859b-fc6d1ec326b3">ProductName</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLLOCATION"></a><a id="installproperty_installlocation"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLLOCATION</b></dt>
</dl>
</td>
<td width="60%">
Installation location. For more information, see 
the <a href="https://msdn.microsoft.com/f4635241-ac18-4bc5-b043-c6e42c0b456e">ARPINSTALLLOCATION</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLSOURCE"></a><a id="installproperty_installsource"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Installation source. For more information, see 
the <a href="https://msdn.microsoft.com/900b26e8-80dd-4e70-8d79-37f09a0c6e86">SourceDir</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LOCALPACKAGE"></a><a id="installproperty_localpackage"></a><dl>
<dt><b>INSTALLPROPERTY_LOCALPACKAGE</b></dt>
</dl>
</td>
<td width="60%">
Local cached package.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_PUBLISHER"></a><a id="installproperty_publisher"></a><dl>
<dt><b>INSTALLPROPERTY_PUBLISHER</b></dt>
</dl>
</td>
<td width="60%">
Publisher. For more information, see 
the <a href="https://msdn.microsoft.com/library/windows/hardware/dn965750">Manufacturer</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_URLINFOABOUT"></a><a id="installproperty_urlinfoabout"></a><dl>
<dt><b>INSTALLPROPERTY_URLINFOABOUT</b></dt>
</dl>
</td>
<td width="60%">
URL information. For more information, see 
the <a href="https://msdn.microsoft.com/5afee7b4-f92d-47ce-adae-31434627d0b7">ARPURLINFOABOUT</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_URLUPDATEINFO"></a><a id="installproperty_urlupdateinfo"></a><dl>
<dt><b>INSTALLPROPERTY_URLUPDATEINFO</b></dt>
</dl>
</td>
<td width="60%">
URL update information. For more information, see 
the <a href="https://msdn.microsoft.com/09c43cb2-e322-407d-ad54-fe93f9be0be3">ARPURLUPDATEINFO</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_VERSIONMINOR"></a><a id="installproperty_versionminor"></a><dl>
<dt><b>INSTALLPROPERTY_VERSIONMINOR</b></dt>
</dl>
</td>
<td width="60%">
Minor product version derived from 
the <a href="https://msdn.microsoft.com/551fca7e-a827-482d-bc56-ff2fe5a17025">ProductVersion</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_VERSIONMAJOR"></a><a id="installproperty_versionmajor"></a><dl>
<dt><b>INSTALLPROPERTY_VERSIONMAJOR</b></dt>
</dl>
</td>
<td width="60%">
Major product version derived from 
the <a href="https://msdn.microsoft.com/551fca7e-a827-482d-bc56-ff2fe5a17025">ProductVersion</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_VERSIONSTRING"></a><a id="installproperty_versionstring"></a><dl>
<dt><b>INSTALLPROPERTY_VERSIONSTRING</b></dt>
</dl>
</td>
<td width="60%">
Product version. For more information, see 
the <a href="https://msdn.microsoft.com/551fca7e-a827-482d-bc56-ff2fe5a17025">ProductVersion</a> property.

</td>
</tr>
</table>
 

To retrieve the product ID, registered owner, or registered company from applications that are installed, set <i>szProperty</i> to one of the following text string values.
					

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>ProductID</td>
<td>The product identifier for the product. For more information, see 
the <a href="https://msdn.microsoft.com/6af23f2d-b22a-470d-b979-da32776e0007">ProductID</a> property.</td>
</tr>
<tr>
<td>RegCompany</td>
<td>The company registered to use this product.</td>
</tr>
<tr>
<td>RegOwner</td>
<td>The owner registered to use this product.</td>
</tr>
</table>
 

To retrieve the instance type of the product, set <i>szProperty</i> to the following value.  This property is available for advertised or installed products.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>InstanceType</td>
<td>A missing value or a value of 0 (zero) indicates a normal product installation.  A value of 1 (one) indicates a product installed using a multiple instance transform and the MSINEWINSTANCE property.   Available with the installer running Windows Server 2003 or Windows XP with SP1.  For more information see, <a href="https://msdn.microsoft.com/5147ecbd-c395-4a8f-972d-f5c5b2173eff">Installing Multiple Instances of Products and Patches</a>.</td>
</tr>
</table>
 

The advertised properties in the following list can be retrieved from applications that are advertised or installed.

<table>
<tr>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>INSTALLPROPERTY_TRANSFORMS</td>
<td>Transforms.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_LANGUAGE</td>
<td>Product language.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_PRODUCTNAME</td>
<td>Human readable product name. For more information, see 
the <a href="https://msdn.microsoft.com/0a9f5be1-9da2-47a7-859b-fc6d1ec326b3">ProductName</a> property.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_ASSIGNMENTTYPE</td>
<td>Equals 0 (zero) if the product is advertised or installed per-user. 


Equals 1 (one) if the product is advertised or installed per-machine for all users.

</td>
</tr>
<tr>
<td>INSTALLPROPERTY_PACKAGECODE</td>
<td>Identifier of the package this product was installed from. For more information, see 
<a href="https://msdn.microsoft.com/dcb6a0d4-e28d-453d-9bda-bfe74f74579b">Package Codes</a>.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_VERSION</td>
<td>Product version derived from 
the <a href="https://msdn.microsoft.com/551fca7e-a827-482d-bc56-ff2fe5a17025">ProductVersion</a> property.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_PRODUCTICON</td>
<td>Primary icon for the package. For more information, see 
the <a href="https://msdn.microsoft.com/4f495029-232c-4aa2-aecf-b400de2e8c4c">ARPPRODUCTICON</a> property.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_PACKAGENAME</td>
<td>Name of the original installation package.</td>
</tr>
<tr>
<td>INSTALLPROPERTY_AUTHORIZED_LUA_APP</td>
<td>A value of one (1) indicates a product that can be serviced by non-administrators using <a href="https://msdn.microsoft.com/f7d64f61-24c8-4037-a10b-d68d0e9e3c42">User Account Control (UAC) Patching</a>. A missing value or a value of 0 (zero) indicates that least-privilege patching is not enabled. Available in Windows Installer 3.0 or later.</td>
</tr>
</table>
 


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
A buffer is too small to hold the requested data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PRODUCT</b></dt>
</dl>
</td>
<td width="60%">
The product is unadvertised or uninstalled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property is unrecognized.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/336a68d6-5239-4313-b6c7-8091907a0e35">MsiGetProductInfo</a> function  returns   ERROR_UNKNOWN_PROPERTY if the application being queried is advertised and not installed.</div>
<div> </div>
</td>
</tr>
</table>
 




## -remarks



When the 
<b>MsiGetProductInfo</b> function returns, the <i>pcchValueBuf</i> parameter contains the length of the string stored in the buffer. The count returned does not include the terminating null character. If the buffer is not large enough, 
<b>MsiGetProductInfo</b> returns ERROR_MORE_DATA and 
<i>pcchValueBuf</i> contains the size of the string, in characters, without counting the null character.

<b>MsiGetProductInfo</b>(INSTALLPROPERTY_LOCALPACKAGE) does not necessarily return a path to the cached package. The cached package is for internal use only. Maintenance mode installations should be invoked through the 
<a href="https://msdn.microsoft.com/067d6fbb-833f-4e0e-bfdb-18d1b8608f58">MsiConfigureFeature</a>, 
<a href="https://msdn.microsoft.com/06f341ac-badd-47a0-af86-4fb76bf528d6">MsiConfigureProduct</a>, or 
<a href="https://msdn.microsoft.com/7a7ae88a-b893-4d10-8542-b2066d1572a9">MsiConfigureProductEx</a> functions.

If you attempt to use <b>MsiGetProductInfo</b> to query an advertised product  for a property that is only available to installed products, the function returns   ERROR_UNKNOWN_PROPERTY. For example, if the application is advertised and not installed, a query for the INSTALLPROPERTY_INSTALLLOCATION property returns an error of ERROR_UNKNOWN_PROPERTY.




## -see-also




<a href="https://msdn.microsoft.com/162bda20-0c62-4eac-8c1f-fd107e42c528">Determining Installation Context</a>



<a href="https://msdn.microsoft.com/850b598a-338e-4f84-8336-01e962256a08">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

