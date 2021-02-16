---
UID: NS:setupapi._SP_NEWDEVICEWIZARD_DATA
title: SP_NEWDEVICEWIZARD_DATA (setupapi.h)
description: An SP_NEWDEVICEWIZARD_DATA structure is used by installers to extend the operation of the hardware installation wizard by adding custom pages. It is used with DIF_NEWDEVICEWIZARD_XXX installation requests.
helpviewer_keywords: ["*PSP_NEWDEVICEWIZARD_DATA","PSP_NEWDEVICEWIZARD_DATA","PSP_NEWDEVICEWIZARD_DATA structure pointer [Device and Driver Installation]","SP_ADDPROPERTYPAGE_DATA","SP_NEWDEVICEWIZARD_DATA","SP_NEWDEVICEWIZARD_DATA structure [Device and Driver Installation]","_SP_NEWDEVICEWIZARD_DATA","devinst.sp_newdevicewizard_data","di-struct_68d6c952-9fca-4d7c-bddb-5e7ceba0117e.xml","setupapi/PSP_NEWDEVICEWIZARD_DATA","setupapi/SP_NEWDEVICEWIZARD_DATA"]
old-location: devinst\sp_newdevicewizard_data.htm
tech.root: devinst
ms.assetid: 9e38ab29-af06-4ca4-b702-fdbed9cd54d4
ms.date: 12/05/2018
ms.keywords: '*PSP_NEWDEVICEWIZARD_DATA, PSP_NEWDEVICEWIZARD_DATA, PSP_NEWDEVICEWIZARD_DATA structure pointer [Device and Driver Installation], SP_ADDPROPERTYPAGE_DATA, SP_NEWDEVICEWIZARD_DATA, SP_NEWDEVICEWIZARD_DATA structure [Device and Driver Installation], _SP_NEWDEVICEWIZARD_DATA, devinst.sp_newdevicewizard_data, di-struct_68d6c952-9fca-4d7c-bddb-5e7ceba0117e.xml, setupapi/PSP_NEWDEVICEWIZARD_DATA, setupapi/SP_NEWDEVICEWIZARD_DATA'
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: SP_NEWDEVICEWIZARD_DATA, *PSP_NEWDEVICEWIZARD_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_NEWDEVICEWIZARD_DATA
 - setupapi/_SP_NEWDEVICEWIZARD_DATA
 - PSP_NEWDEVICEWIZARD_DATA
 - setupapi/PSP_NEWDEVICEWIZARD_DATA
 - SP_NEWDEVICEWIZARD_DATA
 - setupapi/SP_NEWDEVICEWIZARD_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_NEWDEVICEWIZARD_DATA
---

# SP_NEWDEVICEWIZARD_DATA structure


## -description

An SP_NEWDEVICEWIZARD_DATA structure is used by installers to extend the operation of the hardware installation wizard by adding custom pages. It is used with DIF_NEWDEVICEWIZARD_<i>XXX</i> installation requests.

## -struct-fields

### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>.

### -field Flags

Reserved. Must be zero.

### -field DynamicPages

An array of property sheet page handles. An installer can add the handles of custom wizard pages to this array.

### -field NumDynamicPages

The number of pages that are added to the<b> DynamicPages</b> array. 

Because the array index is zero-based, this value is also the index to the next free entry in the array. For example, if there are 3 pages in the array, <b>DynamicPages[</b>3<b>]</b> is the next entry for an installer to use.

### -field hwndWizardDlg

The handle to the top-level window of the hardware installation wizard .

## -remarks

<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_newdevicewizard_data">SP_ADDPROPERTYPAGE_DATA</a> is an alias for this structure.

## -see-also

<a href="/windows-hardware/drivers/install/dif-newdevicewizard-finishinstall">DIF_NEWDEVICEWIZARD_FINISHINSTALL</a>



<a href="/windows-hardware/drivers/install/dif-newdevicewizard-postanalyze">DIF_NEWDEVICEWIZARD_POSTANALYZE</a>



<a href="/windows-hardware/drivers/install/dif-newdevicewizard-preanalyze">DIF_NEWDEVICEWIZARD_PREANALYZE</a>



<a href="/windows-hardware/drivers/install/dif-newdevicewizard-preselect">DIF_NEWDEVICEWIZARD_PRESELECT</a>



<a href="/windows-hardware/drivers/install/dif-newdevicewizard-select">DIF_NEWDEVICEWIZARD_SELECT</a>