---
UID: NE:iads.__MIDL___MIDL_itf_ads_0000_0000_0023
title: ADSI_DIALECT_ENUM (iads.h)
description: The ADSI_DIALECT_ENUM enumeration specifies query dialects used in the OLE DB provider for ADSI.
helpviewer_keywords: ["ADSI_DIALECT_ENUM","ADSI_DIALECT_ENUM enumeration [ADSI]","ADSI_DIALECT_LDAP","ADSI_DIALECT_SQL","_ds_adsi_dialect_enum","adsi.adsi__dialect__enum","adsi.adsi_dialect_enum","iads/ADSI_DIALECT_ENUM","iads/ADSI_DIALECT_LDAP","iads/ADSI_DIALECT_SQL"]
old-location: adsi\adsi_dialect_enum.htm
tech.root: adsi
ms.assetid: 049b9367-c80b-47c2-97d8-b25537a9c0ba
ms.date: 12/05/2018
ms.keywords: ADSI_DIALECT_ENUM, ADSI_DIALECT_ENUM enumeration [ADSI], ADSI_DIALECT_LDAP, ADSI_DIALECT_SQL, _ds_adsi_dialect_enum, adsi.adsi__dialect__enum, adsi.adsi_dialect_enum, iads/ADSI_DIALECT_ENUM, iads/ADSI_DIALECT_LDAP, iads/ADSI_DIALECT_SQL
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
targetos: Windows
req.typenames: ADSI_DIALECT_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0023
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0023
 - ADSI_DIALECT_ENUM
 - iads/ADSI_DIALECT_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADSI_DIALECT_ENUM
---

# ADSI_DIALECT_ENUM enumeration


## -description

The <b>ADSI_DIALECT_ENUM</b> enumeration specifies query dialects used in the OLE DB provider for ADSI.

## -enum-fields

### -field ADSI_DIALECT_LDAP:0

ADSI queries are based on the LDAP dialect.

### -field ADSI_DIALECT_SQL:0x1

ADSI queries are based on the SQL dialect.

## -remarks

An ActiveX Data Object (ADO) client can use one of the two ADSI query dialects to query a directory. For more information about the ADSI query dialects, see <a href="/windows/desktop/ADSI/searching-with-activex-data-objects-ado">Searching with ActiveX Data Objects</a>.

<div class="alert"><b>Note</b>  Because Visual Basic Script (VBScript) cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numerical constants to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>
