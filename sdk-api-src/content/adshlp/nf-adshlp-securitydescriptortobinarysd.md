---
UID: NF:adshlp.SecurityDescriptorToBinarySD
title: SecurityDescriptorToBinarySD function
author: windows-sdk-content
description: Converts an IADsSecurityDescriptor object to the binary security descriptor format.
old-location: adsi\securitydescriptortobinarysd.htm
tech.root: adsi
ms.assetid: b1c814fd-df0f-406b-adfc-c356ce37d524
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SecurityDescriptorToBinarySD, SecurityDescriptorToBinarySD function [ADSI], adshlp/SecurityDescriptorToBinarySD, adsi.securitydescriptortobinarysd
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - SecurityDescriptorToBinarySD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SecurityDescriptorToBinarySD function


## -description


The <b>SecurityDescriptorToBinarySD</b> function converts an <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object to the binary security descriptor format.


## -parameters




### -param vVarSecDes [in]

Type: <b>VARIANT</b>

Contains a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> that contains the security descriptor to convert. The <b>VARIANT</b> must contain a <b>VT_DISPATCH</b> that contains an <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object.


### -param ppSecurityDescriptor [out]

Type: <b>PSECURITY_DESCRIPTOR*</b>

Address of a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> pointer that receives the binary security descriptor data. The caller must free this memory by passing this pointer to the <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a> function.


### -param pdwSDLength [out]

Type: <b>PDWORD</b>

Address of a <b>DWORD</b> value that receives the length, in bytes of the binary security descriptor data.


### -param pszServerName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that specifies the name of the server where the security descriptor is placed. This parameter is optional and can be <b>NULL</b>.


### -param userName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that contains the user name that the security descriptor is associated to. This parameter is optional and can be <b>NULL</b>.


### -param passWord [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that contains the password that the security descriptor is associated. This parameter is optional and can be <b>NULL</b>.


### -param dwFlags [in]

Type: <b>DWORD</b>

Contains authentication flags for the conversion. This can be zero or a combination of one or more of the <a href="https://msdn.microsoft.com/3a45e0c2-5392-456d-80c9-ebd17d056a85">ADS_AUTHENTICATION_ENUM</a> enumeration values.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values, as well as the following.




## -remarks



This function is used for legacy applications to manually convert security descriptors to binary security descriptors. For new applications, use <a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>, which performs this conversion automatically.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/3a45e0c2-5392-456d-80c9-ebd17d056a85">ADS_AUTHENTICATION_ENUM</a>



<a href="https://msdn.microsoft.com/c93d00d2-7155-4bf4-8a65-2412022a2fba">BinarySDToSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a>
 

 

