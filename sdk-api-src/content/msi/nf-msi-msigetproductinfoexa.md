---
UID: NF:msi.MsiGetProductInfoExA
title: MsiGetProductInfoExA function (msi.h)
description: Returns product information for advertised and installed products. (ANSI)
helpviewer_keywords: ["INSTALLPROPERTY_HELPLINK", "INSTALLPROPERTY_HELPTELEPHONE", "INSTALLPROPERTY_INSTALLDATE", "INSTALLPROPERTY_INSTALLEDLANGUAGE", "INSTALLPROPERTY_INSTALLEDPRODUCTNAME", "INSTALLPROPERTY_INSTALLLOCATION", "INSTALLPROPERTY_INSTALLSOURCE", "INSTALLPROPERTY_LOCALPACKAGE", "INSTALLPROPERTY_PRODUCTSTATE", "INSTALLPROPERTY_PUBLISHER", "INSTALLPROPERTY_URLINFOABOUT", "INSTALLPROPERTY_URLUPDATEINFO", "INSTALLPROPERTY_VERSIONMAJOR", "INSTALLPROPERTY_VERSIONMINOR", "INSTALLPROPERTY_VERSIONSTRING", "MSIINSTALLCONTEXT_MACHINE", "MSIINSTALLCONTEXT_USERMANAGED", "MSIINSTALLCONTEXT_USERUNMANAGED", "MsiGetProductInfoExA", "NULL", "User SID", "msi/MsiGetProductInfoExA"]
old-location: setup\msigetproductinfoex.htm
tech.root: setup
ms.assetid: b0060666-3987-49eb-916e-0bcbf54acb23
ms.date: 12/05/2018
ms.keywords: INSTALLPROPERTY_HELPLINK, INSTALLPROPERTY_HELPTELEPHONE, INSTALLPROPERTY_INSTALLDATE, INSTALLPROPERTY_INSTALLEDLANGUAGE, INSTALLPROPERTY_INSTALLEDPRODUCTNAME, INSTALLPROPERTY_INSTALLLOCATION, INSTALLPROPERTY_INSTALLSOURCE, INSTALLPROPERTY_LOCALPACKAGE, INSTALLPROPERTY_PRODUCTSTATE, INSTALLPROPERTY_PUBLISHER, INSTALLPROPERTY_URLINFOABOUT, INSTALLPROPERTY_URLUPDATEINFO, INSTALLPROPERTY_VERSIONMAJOR, INSTALLPROPERTY_VERSIONMINOR, INSTALLPROPERTY_VERSIONSTRING, MSIINSTALLCONTEXT_MACHINE, MSIINSTALLCONTEXT_USERMANAGED, MSIINSTALLCONTEXT_USERUNMANAGED, MsiGetProductInfoEx, MsiGetProductInfoEx function, MsiGetProductInfoExA, MsiGetProductInfoExW, NULL, User SID, msi/MsiGetProductInfoEx, msi/MsiGetProductInfoExA, msi/MsiGetProductInfoExW, setup.msigetproductinfoex
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetProductInfoExW (Unicode) and MsiGetProductInfoExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiGetProductInfoExA
 - msi/MsiGetProductInfoExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiGetProductInfoEx
 - MsiGetProductInfoExA
 - MsiGetProductInfoExW
---

# MsiGetProductInfoExA function


## -description

The <b>MsiGetProductInfoEx</b> function returns product information for advertised and installed products. This function can  retrieve information 


   about an instance of a  product that is installed under a user account other than the current user.

The calling process must have administrative privileges for a user who is different from the current user. The <b>MsiGetProductInfoEx</b> function cannot query an instance of a product  that is advertised under a per-user-unmanaged context for a user account other than the current user.

This function is an extension of the <a href="/windows/desktop/api/msi/nf-msi-msigetproductinfoa">MsiGetProductInfo</a> function.

## -parameters

### -param szProductCode [in]

The <a href="/windows/desktop/Msi/productcode">ProductCode</a> GUID of the product instance that is being queried.

### -param szUserSid [in]

The security identifier (SID) of the account under which the instance of the product that is being queried exists. A <b>NULL</b> specifies the current user SID.

<table>
<tr>
<th>SID</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
</dl>
</td>
<td width="60%">
The currently logged-on user.

</td>
</tr>
<tr>
<td width="40%"><a id="User_SID"></a><a id="user_sid"></a><a id="USER_SID"></a><dl>
<dt><b>User SID</b></dt>
</dl>
</td>
<td width="60%">
The enumeration for a specific user in the system.  An example of user SID is "S-1-3-64-2415071341-1358098788-3127455600-2561".

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The special SID string "S-1-5-18" (system) cannot be used to enumerate products installed as per-machine. If <i>dwContext</i> is "MSIINSTALLCONTEXT_MACHINE", <i>szUserSid</i> must be <b>NULL</b>.</div>
<div> </div>

### -param dwContext [in]

The installation context  of the product instance that is being queried.

<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERMANAGED"></a><a id="msiinstallcontext_usermanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the product property for the per–user–managed instance of the product.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_USERUNMANAGED"></a><a id="msiinstallcontext_userunmanaged"></a><dl>
<dt><b>MSIINSTALLCONTEXT_USERUNMANAGED</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the product property for the per–user–unmanaged instance of the product.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIINSTALLCONTEXT_MACHINE"></a><a id="msiinstallcontext_machine"></a><dl>
<dt><b>MSIINSTALLCONTEXT_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the product property for the per-machine instance of the product.

</td>
</tr>
</table>

### -param szProperty [in]

Property being queried.

The property to be retrieved. The properties in the following table can only be retrieved from applications that are already installed. All required properties are guaranteed to be available, but other properties are available only if the property is set. For more information, see  
<a href="/windows/desktop/Msi/required-properties">Required Properties</a> and <a href="/windows/desktop/Msi/properties">Properties</a>.

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_PRODUCTSTATE"></a><a id="installproperty_productstate"></a><dl>
<dt><b>INSTALLPROPERTY_PRODUCTSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the product returned in string form as "1" for advertised and "5" for installed.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_HELPLINK"></a><a id="installproperty_helplink"></a><dl>
<dt><b>INSTALLPROPERTY_HELPLINK</b></dt>
</dl>
</td>
<td width="60%">
The support link. For more information, see  
the <a href="/windows/desktop/Msi/arphelplink">ARPHELPLINK</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_HELPTELEPHONE"></a><a id="installproperty_helptelephone"></a><dl>
<dt><b>INSTALLPROPERTY_HELPTELEPHONE</b></dt>
</dl>
</td>
<td width="60%">
The support telephone. For more information, see   
the <a href="/windows/desktop/Msi/arphelptelephone">ARPHELPTELEPHONE</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLDATE"></a><a id="installproperty_installdate"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLDATE</b></dt>
</dl>
</td>
<td width="60%">
The last time this product received service. The value of this property is replaced each time a patch is applied or removed from the product or the /v <a href="/windows/desktop/Msi/command-line-options">Command-Line Option</a> is used to repair the product.  If the product has received no repairs or patches this property contains the time this product was installed on this computer.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLEDLANGUAGE"></a><a id="installproperty_installedlanguage"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLEDLANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Installed language.


<b><a href="/windows/desktop/Msi/not-supported-in-windows-installer-4-5">Windows Installer 4.5 and earlier</a>:  </b>Not supported.



</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></a><a id="installproperty_installedproductname"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLEDPRODUCTNAME</b></dt>
</dl>
</td>
<td width="60%">
The installed product name. For more information, see the <a href="/windows/desktop/Msi/productname">ProductName</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLLOCATION"></a><a id="installproperty_installlocation"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLLOCATION</b></dt>
</dl>
</td>
<td width="60%">
The installation location. For more information, see the <a href="/windows/desktop/Msi/arpinstalllocation">ARPINSTALLLOCATION</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_INSTALLSOURCE"></a><a id="installproperty_installsource"></a><dl>
<dt><b>INSTALLPROPERTY_INSTALLSOURCE</b></dt>
</dl>
</td>
<td width="60%">
The installation source. For more information, see  
the <a href="/windows/desktop/Msi/sourcedir">SourceDir</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_LOCALPACKAGE"></a><a id="installproperty_localpackage"></a><dl>
<dt><b>INSTALLPROPERTY_LOCALPACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The local cached package.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_PUBLISHER"></a><a id="installproperty_publisher"></a><dl>
<dt><b>INSTALLPROPERTY_PUBLISHER</b></dt>
</dl>
</td>
<td width="60%">
The publisher. For more information, see the <a href="/windows/desktop/Msi/manufacturer">Manufacturer</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_URLINFOABOUT"></a><a id="installproperty_urlinfoabout"></a><dl>
<dt><b>INSTALLPROPERTY_URLINFOABOUT</b></dt>
</dl>
</td>
<td width="60%">
URL information. For more information, see the <a href="/windows/desktop/Msi/arpurlinfoabout">ARPURLINFOABOUT</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_URLUPDATEINFO"></a><a id="installproperty_urlupdateinfo"></a><dl>
<dt><b>INSTALLPROPERTY_URLUPDATEINFO</b></dt>
</dl>
</td>
<td width="60%">
The URL update information. For more information, see  
the <a href="/windows/desktop/Msi/arpurlupdateinfo">ARPURLUPDATEINFO</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_VERSIONMINOR"></a><a id="installproperty_versionminor"></a><dl>
<dt><b>INSTALLPROPERTY_VERSIONMINOR</b></dt>
</dl>
</td>
<td width="60%">
The minor product version that is derived from 
the <a href="/windows/desktop/Msi/productversion">ProductVersion</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_VERSIONMAJOR"></a><a id="installproperty_versionmajor"></a><dl>
<dt><b>INSTALLPROPERTY_VERSIONMAJOR</b></dt>
</dl>
</td>
<td width="60%">
The major product version that is derived from 
the <a href="/windows/desktop/Msi/productversion">ProductVersion</a> property.

</td>
</tr>
<tr>
<td width="40%"><a id="INSTALLPROPERTY_VERSIONSTRING"></a><a id="installproperty_versionstring"></a><dl>
<dt><b>INSTALLPROPERTY_VERSIONSTRING</b></dt>
</dl>
</td>
<td width="60%">
The product version. For more information, see 
the <a href="/windows/desktop/Msi/productversion">ProductVersion</a> property.

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
<td>The product identifier. For more information, see  
the <a href="/windows/desktop/Msi/productid">ProductID</a> property.</td>
</tr>
<tr>
<td>RegCompany</td>
<td>The company that is registered to use the product.</td>
</tr>
<tr>
<td>RegOwner</td>
<td>The owner who is registered to use the product.</td>
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
<td>A missing value or a value of 0 (zero) indicates a normal product installation.  A value of one (1) indicates a product installed using a multiple instance transform and the <a href="/windows/desktop/Msi/msinewinstance">MSINEWINSTANCE</a> property.   For more information, see <a href="/windows/desktop/Msi/installing-multiple-instances-of-products-and-patches">Installing Multiple Instances of Products and Patches</a>.</td>
</tr>
</table>
 

The properties in the following table can be retrieved from applications that are advertised or installed. These properties cannot be retrieved for product instances that are installed under a per-user-unmanaged context for user accounts other than current user account.

<table>
<tr>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td><b>INSTALLPROPERTY_TRANSFORMS</b></td>
<td>Transforms.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_LANGUAGE</b></td>
<td>Product language.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_PRODUCTNAME</b></td>
<td>Human readable product name. For more information, see  
the <a href="/windows/desktop/Msi/productname">ProductName</a> property.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_ASSIGNMENTTYPE</b></td>
<td>Equals 0 (zero) if the product is advertised or installed per-user. 


Equals one (1) if the product is advertised or installed per-computer for all users.

</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_PACKAGECODE</b></td>
<td>Identifier of the package that  a product is installed from. For more information, see the <a href="/windows/desktop/Msi/package-codes">Package Codes</a> property.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_VERSION</b></td>
<td>Product version derived from 
the <a href="/windows/desktop/Msi/productversion">ProductVersion</a> property.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_PRODUCTICON</b></td>
<td>Primary icon for the package. For more information, see  
the <a href="/windows/desktop/Msi/arpproducticon">ARPPRODUCTICON</a> property.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_PACKAGENAME</b></td>
<td>Name of the original installation package.</td>
</tr>
<tr>
<td><b>INSTALLPROPERTY_AUTHORIZED_LUA_APP</b></td>
<td>A value of one (1) indicates a product that can be serviced by non-administrators using <a href="/windows/desktop/Msi/user-account-control--uac--patching">User Account Control (UAC) Patching</a>. A missing value or a value of 0 (zero) indicates that least-privilege patching is not enabled. Available in Windows Installer 3.0 or later.</td>
</tr>
</table>

### -param szValue [out, optional]

A pointer to a  buffer that receives the property value. This buffer should be large enough to contain the information. If the buffer is too small, the function returns <b>ERROR_MORE_DATA</b> and sets *<i>pcchValue</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.

If <i>lpValue</i> is set to <b>NULL</b> and <i>pcchValue</i> is set to a valid pointer,  the function returns <b>ERROR_SUCCESS</b> and sets *<i>pcchValue</i> to the number of <b>TCHAR</b> in the value, not including the terminating NULL character.  The function can then be called again to retrieve the value, with <i>lpValue</i> buffer large enough to contain *<i>pcchValue</i> + 1 characters.

If <i>lpValue</i> and <i>pcchValue</i> are both set to <b>NULL</b>, the function returns <b>ERROR_SUCCESS</b> if the value exists, without  retrieving the value.

### -param pcchValue [in, out, optional]

A pointer to a variable that specifies the number of <b>TCHAR</b> in the <i>lpValue</i> buffer. When the function returns, this parameter is set to the size of the requested value whether or not the function copies the value into the specified buffer. The size is returned as the number of <b>TCHAR</b> in the requested value, not including the terminating null character.

This parameter can be set to <b>NULL</b> only if <i>lpValue</i> is also <b>NULL</b>. Otherwise, the function returns <b>ERROR_INVALID_PARAMETER</b>.

## -returns

The <b>MsiGetProductInfoEx</b> function returns the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process must have administrative privileges to get information for a product installed for a user other than the current user.

</td>
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
An invalid parameter is passed to the function.

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

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/msi/nf-msi-msigetproductinfoa">MsiGetProductInfo</a> function returns   <b>ERROR_UNKNOWN_PROPERTY</b> if the application being queried is advertised and not installed.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected internal failure.

</td>
</tr>
</table>

## -remarks

When the 
<b>MsiGetProductInfoEx</b> function returns, the <i>pcchValue</i> parameter contains the length of the string that is stored in the buffer. The count returned does not include the terminating null character. If the buffer is not big enough, 
<b>MsiGetProductInfoEx</b> returns <b>ERROR_MORE_DATA</b>, and 
the <i>pcchValue</i> parameter contains the size of the string, in <b>TCHAR</b>, without counting the null character.

The <b>MsiGetProductInfoEx</b> function  (<b>INSTALLPROPERTY_LOCALPACKAGE</b>) returns a path to the cached package. The cached package is for internal use only. Maintenance mode installations must be invoked through the 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a>, 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a>, or 
<a href="/windows/desktop/api/msi/nf-msi-msiconfigureproductexa">MsiConfigureProductEx</a> functions.

The <a href="/windows/desktop/api/msi/nf-msi-msigetproductinfoa">MsiGetProductInfo</a> function returns   <b>ERROR_UNKNOWN_PROPERTY</b> if the application being queried is advertised and not installed.  For example, if the application is advertised and not installed, a query for <b>INSTALLPROPERTY_INSTALLLOCATION</b> returns an error of <b>ERROR_UNKNOWN_PROPERTY</b>.





> [!NOTE]
> The msi.h header defines MsiGetProductInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/arphelplink">ARPHELPLINK</a>



<a href="/windows/desktop/Msi/arphelptelephone">ARPHELPTELEPHONE</a>



<a href="/windows/desktop/Msi/arpinstalllocation">ARPINSTALLLOCATION</a>



<a href="/windows/desktop/Msi/arpproducticon">ARPPRODUCTICON</a>



<a href="/windows/desktop/Msi/arpurlinfoabout">ARPURLINFOABOUT</a>



<a href="/windows/desktop/Msi/arpurlupdateinfo">ARPURLUPDATEINFO</a>



<a href="/windows/desktop/Msi/manufacturer">Manufacturer</a>



<a href="/windows/desktop/api/msi/nf-msi-msiconfigurefeaturea">MsiConfigureFeature</a>



<a href="/windows/desktop/api/msi/nf-msi-msiconfigureproducta">MsiConfigureProduct</a>



<a href="/windows/desktop/api/msi/nf-msi-msiconfigureproductexa">MsiConfigureProductEx</a>



<a href="/windows/desktop/Msi/not-supported-in-windows-installer-version-2-0">Not Supported in Windows Installer 2.0 and earlier</a>



<a href="/windows/desktop/Msi/package-codes">Package Codes</a>



<a href="/windows/desktop/Msi/productcode">ProductCode</a>



<a href="/windows/desktop/Msi/productid">ProductID</a>



<a href="/windows/desktop/Msi/productname">ProductName</a>



<a href="/windows/desktop/Msi/productversion">ProductVersion</a>



<a href="/windows/desktop/Msi/properties">Properties</a>



<a href="/windows/desktop/Msi/required-properties">Required Properties</a>



<a href="/windows/desktop/Msi/sourcedir">SourceDir</a>



<a href="/windows/desktop/Msi/installer-function-reference">System Status Functions</a>
