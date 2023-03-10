---
UID: NN:devicetopology.IKsJackDescription
title: IKsJackDescription (devicetopology.h)
description: The IKsJackDescription interface provides information about the jacks or internal connectors that provide a physical connection between a device on an audio adapter and an external or internal endpoint device (for example, a microphone or CD player).
helpviewer_keywords: ["IKsJackDescription","IKsJackDescription interface [Core Audio]","IKsJackDescription interface [Core Audio]","described","coreaudio.iksjackdescription","devicetopology/IKsJackDescription"]
old-location: coreaudio\iksjackdescription.htm
tech.root: CoreAudio
ms.assetid: 0ca9e719-7179-4302-99ff-df137141f58f
ms.date: 12/05/2018
ms.keywords: IKsJackDescription, IKsJackDescription interface [Core Audio], IKsJackDescription interface [Core Audio],described, coreaudio.iksjackdescription, devicetopology/IKsJackDescription
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKsJackDescription
 - devicetopology/IKsJackDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IKsJackDescription
---

# IKsJackDescription interface


## -description

The <b>IKsJackDescription</b> interface provides information about the jacks or internal connectors that provide a physical connection between a device on an audio adapter and an external or internal endpoint device (for example, a microphone or CD player). The client obtains a reference to the <b>IKsJackDescription</b> interface of a part by calling the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method with parameter <i>refiid</i> set to <b>REFIID</b> IID_IKsJackDescription. The call to <b>IPart::Activate</b> succeeds only if the part supports the <b>IKsJackDescription</b> interface. Only a part object that represents a connector with a Physical_External or Physical_Internal connection type will support this interface.

Most Windows audio adapter drivers support the Windows Driver Model (WDM) and use kernel-streaming (KS) properties to represent the hardware description parameters in connectors (referred to as KS pins). The <b>IKsJackDescription</b> interface provides convenient access to the KSPROPERTY_JACK_DESCRIPTION property of a connector to an endpoint device. For more information about KS properties and KS pins, see the Windows DDK documentation.

## -inheritance

The <b>IKsJackDescription</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IKsJackDescription</b> also has these types of members:

## -remarks

If an audio endpoint device supports the <b>IKsJackDescription</b> interface, the Windows multimedia control panel, Mmsys.cpl, displays the jack information. To view the jack information, follow these steps:

<ol>
<li>
To run Mmsys.cpl, open a Command Prompt window and enter the following command:

<b>control mmsys.cpl</b>

Alternatively, you can run Mmsys.cpl by right-clicking the speaker icon in the notification area, which is located on the right side of the taskbar, and selecting either <b>Playback Devices</b> or <b>Recording Devices</b>.

</li>
<li>
After the Mmsys.cpl window opens, select a device from either the list of playback devices or the list of recording devices, and click <b>Properties</b>.

</li>
<li>
When the properties window opens, click <b>General</b>. If the selected property page displays the jack information for the device, the device supports the <b>IKsJackDescription</b> interface. If the property page displays the text "No jack information is available", the device does not support the interface.

</li>
</ol>
The following code example shows how to obtain the <b>IKsJackDescription</b> interface for an audio endpoint device:


```cpp
//-----------------------------------------------------------
// Get the IKsJackDescription interface that describes the
// audio jack or jacks that the endpoint device plugs into.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetJackInfo(IMMDevice *pDevice,
                    IKsJackDescription **ppJackDesc)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPart = NULL;
    IKsJackDescription *pJackDesc = NULL;

    if (NULL != ppJackDesc)
    {
        *ppJackDesc = NULL;
    }
    if (NULL == pDevice || NULL == ppJackDesc)
    {
        return E_POINTER;
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pDevice->Activate(__uuidof(IDeviceTopology), CLSCTX_ALL,
                           NULL, (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    EXIT_ON_ERROR(hr)

    // Step across the connection to the jack on the adapter.
    hr = pConnFrom->GetConnectedTo(&pConnTo);
    if (HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND) == hr)
    {
        // The adapter device is not currently active.
        hr = E_NOINTERFACE;
    }
    EXIT_ON_ERROR(hr)

    // Get the connector's IPart interface.
    hr = pConnTo->QueryInterface(__uuidof(IPart), (void**)&pPart);
    EXIT_ON_ERROR(hr)

    // Activate the connector's IKsJackDescription interface.
    hr = pPart->Activate(CLSCTX_INPROC_SERVER,
                         __uuidof(IKsJackDescription), (void**)&pJackDesc);
    EXIT_ON_ERROR(hr)

    *ppJackDesc = pJackDesc;

Exit:
    SAFE_RELEASE(pDeviceTopology)
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPart)
    return hr;
}

```


In the preceding code example, the GetJackInfo function takes two parameters. Input parameter <i>pDevice</i> points to the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface of an endpoint device. Output parameter <i>ppJackDesc</i> points to a pointer value into which the function writes the address of the corresponding <b>IKsJackDescription</b> interface, if the interface exists. If the interface does not exist, the function writes <b>NULL</b> to  <i>*ppJackDesc</i> and returns error code E_NOINTERFACE.

In the preceding code example, the call to <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> retrieves the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-idevicetopology">IDeviceTopology</a> interface of the endpoint device. The device topology of an endpoint device contains a single connector (connector number 0) that connects to the adapter device. At the other side of this connection, the connector on the adapter device represents the audio jack or jacks that the endpoint device plugs into. The call to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-idevicetopology-getconnector">IDeviceTopology::GetConnector</a> method retrieves the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> interface of the connector on the endpoint device, and the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getconnectedto">IConnector::GetConnectedTo</a> method call retrieves the corresponding connector on the adapter device. Finally, the <b>IConnector::QueryInterface</b> method call retrieves the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-ipart">IPart</a> interface of the adapter device's connector, and the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a> method call retrieves the connector's <b>IKsJackDescription</b> interface, if it exists.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/CoreAudio/devicetopology-api">DeviceTopology API</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-ipart-activate">IPart::Activate</a>
