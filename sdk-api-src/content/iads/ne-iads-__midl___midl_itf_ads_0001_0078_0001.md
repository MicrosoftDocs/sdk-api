---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0078_0001
title: "__MIDL___MIDL_itf_ads_0001_0078_0001"
author: windows-sdk-content
description: The ADS_SETTYPE_ENUM enumeration specifies the available pathname format used by the IADsPathname::Set method.
old-location: adsi\ads_settype_enum.htm
old-project: ADSI
ms.assetid: fbf7de54-3ea7-4d66-ad56-21cae1e28c07
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ADS_SETTYPE_DN, ADS_SETTYPE_ENUM, ADS_SETTYPE_ENUM enumeration [ADSI], ADS_SETTYPE_FULL, ADS_SETTYPE_PROVIDER, ADS_SETTYPE_SERVER, __MIDL___MIDL_itf_ads_0001_0078_0001, _ds_ads_settype_enum, adsi.ads__settype__enum, adsi.ads_settype_enum, iads/ADS_SETTYPE_DN, iads/ADS_SETTYPE_ENUM, iads/ADS_SETTYPE_FULL, iads/ADS_SETTYPE_PROVIDER, iads/ADS_SETTYPE_SERVER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADS_SETTYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SETTYPE_ENUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_ads_0001_0078_0001 enumeration


## -description


The <b>ADS_SETTYPE_ENUM</b> enumeration specifies the available pathname format used by the  <a href="https://msdn.microsoft.com/1672c1b0-1008-41e7-8ca4-eefb559f523d">IADsPathname::Set</a> method.


## -enum-fields




### -field ADS_SETTYPE_FULL

Sets the full path, for example, "LDAP://servername/o=internet/…/cn=bar".


### -field ADS_SETTYPE_PROVIDER

Updates the provider only, for example, "LDAP".


### -field ADS_SETTYPE_SERVER

Updates the server name only, for example, "servername".


### -field ADS_SETTYPE_DN

Updates the distinguished name only, for example, "o=internet/…/cn=bar".


## -remarks



Since VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/1672c1b0-1008-41e7-8ca4-eefb559f523d">IADsPathname::Set</a>
 

 

