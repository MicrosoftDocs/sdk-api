---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _SP_PROPSHEETPAGE_REQUEST structure


## -description


An SP_PROPSHEETPAGE_REQUEST structure can be passed as the first parameter (<i>lpv</i>) to the <b>ExtensionPropSheetPageProc</b> entry point in the <a href="devinst.setupapi">SetupAPI</a> DLL. <b>ExtensionPropSheetPageProc</b> is used to retrieve a handle to a specified property sheet page.

For information about <b>ExtensionPropSheetPageProc</b> and related functions, see the Microsoft Windows SDK documentation.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_PROPSHEETPAGE_REQUEST structure. 


### -field PageRequested

The property sheet page to add to the property sheet. Can be one of the following values:





#### SPPSR_SELECT_DEVICE_RESOURCES

Specifies the Resource Selection page supplied by the SetupAPI DLL. 



#### SPPSR_ENUM_BASIC_DEVICE_PROPERTIES

Specifies a page that is supplied by the device's BasicProperties32 provider. That is, an installer or other component that supplied page(s) in response to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543659">DIF_ADDPROPERTYPAGE_BASIC</a> installation request. 



#### SPPSR_ENUM_ADV_DEVICE_PROPERTIES

Specifies a page that is supplied by the class and/or the device's EnumPropPages32 provider. That is, an installer or other component that supplied page(s) in response to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543656">DIF_ADDPROPERTYPAGE_ADVANCED</a> installation request.


### -field DeviceInfoSet

The handle for the device information set that contains the device being installed.


### -field DeviceInfoData

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure for the device being installed.


## -remarks



The component that is retrieving the property pages calls SetupAPI's <b>ExtensionPropSheetPageProc</b> function and passes in a pointer to a SP_PROPSHEETPAGE_REQUEST structure, the address of their  <b>AddPropSheetPageProc </b>function, and some private data. The property sheet provider calls the <b>AddPropSheetPageProc</b> routine for each property sheet it provides. 

The following code excerpt shows how to retrieve one page, the SetupAPI's Resource Selection page:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>{
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

        if(!PropSheetExtProc(&amp;PropPageRequest, 
                AddPropSheetPageProc, &amp;hPages[1])) {
            Err = ERROR_INVALID_PARAMETER;
            FreeLibrary(hLib);
            return Err;
        }
        .
        .
        .
}</pre>
</td>
</tr>
</table></span></div>
The <b>AddPropSheetPageProc</b> for the previous excerpt would be something like the following:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>BOOL
CALLBACK
AddPropSheetPageProc(
    IN HPROPSHEETPAGE hpage,
    IN LPARAM lParam
   )
{
    *((HPROPSHEETPAGE *)lParam) = hpage;
    return TRUE;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543656">DIF_ADDPROPERTYPAGE_ADVANCED</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543659">DIF_ADDPROPERTYPAGE_BASIC</a>
 

 

