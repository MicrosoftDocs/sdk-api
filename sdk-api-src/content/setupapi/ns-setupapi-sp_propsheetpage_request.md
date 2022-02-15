---
UID: NS:setupapi._SP_PROPSHEETPAGE_REQUEST
title: SP_PROPSHEETPAGE_REQUEST (setupapi.h)
description: An SP_PROPSHEETPAGE_REQUEST structure can be passed as the first parameter (lpv) to the ExtensionPropSheetPageProc entry point in the SetupAPI DLL.
helpviewer_keywords: ["*PSP_PROPSHEETPAGE_REQUEST","PSP_PROPSHEETPAGE_REQUEST","PSP_PROPSHEETPAGE_REQUEST structure pointer [Device and Driver Installation]","SP_PROPSHEETPAGE_REQUEST","SP_PROPSHEETPAGE_REQUEST structure [Device and Driver Installation]","devinst.sp_propsheetpage_request","di-struct_03c50681-4081-4ae3-88ba-32a10e937207.xml","setupapi/PSP_PROPSHEETPAGE_REQUEST","setupapi/SP_PROPSHEETPAGE_REQUEST"]
old-location: devinst\sp_propsheetpage_request.htm
tech.root: devinst
ms.assetid: f9a4e685-e396-4b2f-a452-14389eb44620
ms.date: 12/05/2018
ms.keywords: '*PSP_PROPSHEETPAGE_REQUEST, PSP_PROPSHEETPAGE_REQUEST, PSP_PROPSHEETPAGE_REQUEST structure pointer [Device and Driver Installation], SP_PROPSHEETPAGE_REQUEST, SP_PROPSHEETPAGE_REQUEST structure [Device and Driver Installation], devinst.sp_propsheetpage_request, di-struct_03c50681-4081-4ae3-88ba-32a10e937207.xml, setupapi/PSP_PROPSHEETPAGE_REQUEST, setupapi/SP_PROPSHEETPAGE_REQUEST'
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
req.typenames: SP_PROPSHEETPAGE_REQUEST, *PSP_PROPSHEETPAGE_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_PROPSHEETPAGE_REQUEST
 - setupapi/_SP_PROPSHEETPAGE_REQUEST
 - PSP_PROPSHEETPAGE_REQUEST
 - setupapi/PSP_PROPSHEETPAGE_REQUEST
 - SP_PROPSHEETPAGE_REQUEST
 - setupapi/SP_PROPSHEETPAGE_REQUEST
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
 - SP_PROPSHEETPAGE_REQUEST
---

# SP_PROPSHEETPAGE_REQUEST structure


## -description

An SP_PROPSHEETPAGE_REQUEST structure can be passed as the first parameter (<i>lpv</i>) to the <b>ExtensionPropSheetPageProc</b> entry point in the <a href="/windows-hardware/drivers/install/setupapi">SetupAPI</a> DLL. <b>ExtensionPropSheetPageProc</b> is used to retrieve a handle to a specified property sheet page.

For information about <b>ExtensionPropSheetPageProc</b> and related functions, see the Microsoft Windows SDK documentation.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_PROPSHEETPAGE_REQUEST structure.

### -field PageRequested

The property sheet page to add to the property sheet. Can be one of the following values:





#### SPPSR_SELECT_DEVICE_RESOURCES

Specifies the Resource Selection page supplied by the SetupAPI DLL. 



#### SPPSR_ENUM_BASIC_DEVICE_PROPERTIES

Specifies a page that is supplied by the device's BasicProperties32 provider. That is, an installer or other component that supplied page(s) in response to a <a href="/windows-hardware/drivers/install/dif-addpropertypage-basic">DIF_ADDPROPERTYPAGE_BASIC</a> installation request. 



#### SPPSR_ENUM_ADV_DEVICE_PROPERTIES

Specifies a page that is supplied by the class and/or the device's EnumPropPages32 provider. That is, an installer or other component that supplied page(s) in response to a <a href="/windows-hardware/drivers/install/dif-addpropertypage-advanced">DIF_ADDPROPERTYPAGE_ADVANCED</a> installation request.

### -field DeviceInfoSet

The handle for the device information set that contains the device being installed.

### -field DeviceInfoData

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for the device being installed.

## -remarks

The component that is retrieving the property pages calls SetupAPI's <b>ExtensionPropSheetPageProc</b> function and passes in a pointer to a SP_PROPSHEETPAGE_REQUEST structure, the address of their  <b>AddPropSheetPageProc </b> function, and some private data. The property sheet provider calls the <b>AddPropSheetPageProc</b> routine for each property sheet it provides. 

The following code excerpt shows how to retrieve one page, the SetupAPI's Resource Selection page:


```
{
    DWORD Err;
    HINSTANCE hLib;
    FARPROC PropSheetExtProc;
    HPROPSHEETPAGE hPages[2];
    .
    .
    .
        if(!(hLib = GetModuleHandle(TEXT("setupapi.dll")))) {
            return GetLastError();
        }

        if(!(PropSheetExtProc = GetProcAddress(hLib,
                 "ExtensionPropSheetPageProc"))) {
            Err = GetLastError();
            FreeLibrary(hLib);
            return Err;
        }

        PropPageRequest.cbSize = sizeof(SP_PROPSHEETPAGE_REQUEST);
        PropPageRequest.PageRequested  = 
            SPPSR_SELECT_DEVICE_RESOURCES;
        PropPageRequest.DeviceInfoSet  = DeviceInfoSet;
        PropPageRequest.DeviceInfoData = DeviceInfoData;

        if(!PropSheetExtProc(&PropPageRequest, 
                AddPropSheetPageProc, &hPages[1])) {
            Err = ERROR_INVALID_PARAMETER;
            FreeLibrary(hLib);
            return Err;
        }
        .
        .
        .
}
```


The <b>AddPropSheetPageProc</b> for the previous excerpt would be something like the following:


```
BOOL
CALLBACK
AddPropSheetPageProc(
    IN HPROPSHEETPAGE hpage,
    IN LPARAM lParam
   )
{
    *((HPROPSHEETPAGE *)lParam) = hpage;
    return TRUE;
}
```

## -see-also

<a href="/windows-hardware/drivers/install/dif-addpropertypage-advanced">DIF_ADDPROPERTYPAGE_ADVANCED</a>



<a href="/windows-hardware/drivers/install/dif-addpropertypage-basic">DIF_ADDPROPERTYPAGE_BASIC</a>