---
UID: NF:adshlp.BinarySDToSecurityDescriptor
title: BinarySDToSecurityDescriptor function
author: windows-sdk-content
description: Converts a binary security descriptor to an IADsSecurityDescriptor object.
old-location: adsi\binarysdtosecuritydescriptor.htm
tech.root: adsi
ms.assetid: c93d00d2-7155-4bf4-8a65-2412022a2fba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BinarySDToSecurityDescriptor, BinarySDToSecurityDescriptor function [ADSI], adshlp/BinarySDToSecurityDescriptor, adsi.binarysdtosecuritydescriptor
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
 - BinarySDToSecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BinarySDToSecurityDescriptor function


## -description


The <b>BinarySDToSecurityDescriptor</b> function converts a binary security descriptor to an <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object.


## -parameters




### -param pSecurityDescriptor [in]

Type: <b>PSECURITY_DESCRIPTOR</b>

Address of a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure to convert.


### -param pVarsec [out]

Type: <b>VARIANT*</b>

Address of a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> that receives the object. The <b>VARIANT</b> contains a <b>VT_DISPATCH</b> object that can be queried for the <a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> interface. The caller must release this <b>VARIANT</b> by passing the <b>VARIANT</b> to the <a href="https://msdn.microsoft.com/en-us/library/ms221165(v=VS.85).aspx">VariantClear</a> function.


### -param pszServerName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that provides the name of the server that the security descriptor was retrieved from. This parameter is optional and can be <b>NULL</b>.


### -param userName [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that provides the user name to be associated with the security descriptor. This parameter is optional and can be <b>NULL</b>.


### -param passWord [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that provides the password to be associated with the security descriptor. This parameter is optional and can be <b>NULL</b>.


### -param dwFlags [in]

Type: <b>DWORD</b>

Contains authentication flags for the conversion. This can be zero or a combination of one or more of the <a href="https://msdn.microsoft.com/3a45e0c2-5392-456d-80c9-ebd17d056a85">ADS_AUTHENTICATION_ENUM</a> enumeration values.


## -returns



Type: <b>HRESULT</b>

This method supports  standard return values, as well as the following:

If the operation fails, an ADSI error code is returned. For more information, see <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



This function is used for legacy applications that must  manually convert security descriptors to binary security descriptors. For new applications, use the <a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a> interface, which does this conversion automatically.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/3a45e0c2-5392-456d-80c9-ebd17d056a85">ADS_AUTHENTICATION_ENUM</a>



<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/781eda1e-1f13-4bb4-ae8e-c9bf4c08e125">IADsSecurityUtility</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/b1c814fd-df0f-406b-adfc-c356ce37d524">SecurityDescriptorToBinarySD</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221165(v=VS.85).aspx">VariantClear</a>
 

 

