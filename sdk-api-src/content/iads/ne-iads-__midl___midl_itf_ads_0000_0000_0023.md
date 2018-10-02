---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0023
title: "__MIDL___MIDL_itf_ads_0000_0000_0023"
author: windows-sdk-content
description: The ADSI_DIALECT_ENUM enumeration specifies query dialects used in the OLE DB provider for ADSI.
old-location: adsi\adsi_dialect_enum.htm
tech.root: ADSI
ms.assetid: 049b9367-c80b-47c2-97d8-b25537a9c0ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ADSI_DIALECT_ENUM, ADSI_DIALECT_ENUM enumeration [ADSI], ADSI_DIALECT_LDAP, ADSI_DIALECT_SQL, __MIDL___MIDL_itf_ads_0000_0000_0023, _ds_adsi_dialect_enum, adsi.adsi__dialect__enum, adsi.adsi_dialect_enum, iads/ADSI_DIALECT_ENUM, iads/ADSI_DIALECT_LDAP, iads/ADSI_DIALECT_SQL
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADSI_DIALECT_ENUM
product: Windows
targetos: Windows
req.typenames: ADSI_DIALECT_ENUM
req.redist: 
---

# __MIDL___MIDL_itf_ads_0000_0000_0023 enumeration


## -description


The <b>ADSI_DIALECT_ENUM</b> enumeration specifies query dialects used in the OLE DB provider for ADSI.


## -enum-fields




### -field ADSI_DIALECT_LDAP

ADSI queries are based on the LDAP dialect.


### -field ADSI_DIALECT_SQL

ADSI queries are based on the SQL dialect.


## -remarks



An ActiveX Data Object (ADO) client can use one of the two ADSI query dialects to query a directory. For more information about the ADSI query dialects, see <a href="https://msdn.microsoft.com/27298f53-a652-49f2-a6e6-d92c7c6022af">Searching with ActiveX Data Objects</a>.

<div class="alert"><b>Note</b>  Because Visual Basic Script (VBScript) cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>
 

 

