---
UID: NS:winuser.tagRAWKEYBOARD
title: RAWKEYBOARD (winuser.h)
description: Contains information about the state of the keyboard.
old-location: inputdev\rawkeyboard.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputstructures\rawkeyboard.htm
ms.date: 12/05/2018
ms.keywords: '*LPRAWKEYBOARD, *PRAWKEYBOARD, LPRAWKEYBOARD, LPRAWKEYBOARD structure pointer [Keyboard and Mouse Input], PRAWKEYBOARD, PRAWKEYBOARD structure pointer [Keyboard and Mouse Input], RAWKEYBOARD, RAWKEYBOARD structure [Keyboard and Mouse Input], RI_KEY_BREAK, RI_KEY_E0, RI_KEY_E1, RI_KEY_MAKE, _win32_RAWKEYBOARD_str, _win32_rawkeyboard_str_cpp, inputdev.rawkeyboard, winui._win32_rawkeyboard_str, winuser/LPRAWKEYBOARD, winuser/PRAWKEYBOARD, winuser/RAWKEYBOARD'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: RAWKEYBOARD, *PRAWKEYBOARD, *LPRAWKEYBOARD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRAWKEYBOARD
 - winuser/tagRAWKEYBOARD
 - PRAWKEYBOARD
 - winuser/PRAWKEYBOARD
 - RAWKEYBOARD
 - winuser/RAWKEYBOARD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - RAWKEYBOARD
---

# RAWKEYBOARD structure


## -description

Contains information about the state of the keyboard.

## -struct-fields

### -field MakeCode

Type: <b>USHORT</b>

Specifies the [scan code](/windows/win32/inputdev/about-keyboard-input#scan-codes) associated with a key press. See Remarks.

### -field Flags

Type: <b>USHORT</b>

Flags for scan code information. It can be one or more of the following:

| Value                | Meaning                          |
|----------------------|----------------------------------|
| **RI\_KEY\_MAKE** 0  | The key is down.                 |
| **RI\_KEY\_BREAK** 1 | The key is up.                   |
| **RI\_KEY\_E0** 2    | The scan code has the E0 prefix. |
| **RI\_KEY\_E1** 4    | The scan code has the E1 prefix. |

### -field Reserved

Type: <b>USHORT</b>

Reserved; must be zero.

### -field VKey

Type: <b>USHORT</b>

The corresponding [legacy virtual-key code](/windows/win32/inputdev/virtual-key-codes).

### -field Message

Type: <b>UINT</b>

The corresponding [legacy keyboard window message](/windows/win32/inputdev/keyboard-input-notifications), for example [WM_KEYDOWN](/windows/win32/inputdev/wm-keydown), [WM_SYSKEYDOWN](/windows/win32/inputdev/wm-syskeydown), and so forth.

### -field ExtraInformation

Type: <b>ULONG</b>

The device-specific additional information for the event.

## -remarks

<b>KEYBOARD_OVERRUN_MAKE_CODE</b> is a special **MakeCode** value sent when an invalid or unrecognizable combination of keys is pressed or the number of keys pressed exceeds the limit for this keyboard.

```cpp
case WM_INPUT:
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEKEYBOARD)
    {
        RAWKEYBOARD& keyboard = raw->data.keyboard;
        WORD scanCode = 0;
        BOOL keyUp = keyboard.Flags & RI_KEY_BREAK;

        // Ignore key overrun state and keys not mapped to any virtual key code
        if (keyboard.MakeCode == KEYBOARD_OVERRUN_MAKE_CODE || keyboard.VKey >= UCHAR_MAX)
            return 0;

        if (keyboard.MakeCode)
        {
            // Compose the full scan code value with its extended byte
            scanCode = MAKEWORD(keyboard.MakeCode & 0x7f, ((keyboard.Flags & RI_KEY_E0) ? 0xe0 : ((keyboard.Flags & RI_KEY_E1) ? 0xe1 : 0x00)));
        }
        else
        {
            // Scan code value may be empty for some buttons (for example multimedia buttons)
            // Try to get the scan code from the virtual key code
            scanCode = LOWORD(MapVirtualKey(keyboard.VKey, MAPVK_VK_TO_VSC_EX));
        }

        // Get the key name for debug output
        TCHAR keyNameBuffer[MAX_PATH] = {};
        GetKeyNameText((LONG)MAKELPARAM(0, (HIBYTE(scanCode) ? KF_EXTENDED : 0x00) | LOBYTE(scanCode)), keyNameBuffer, MAX_PATH);

        // Debug output
        TCHAR printBuffer[MAX_PATH] = {};
        StringCchPrintf(printBuffer, MAX_PATH, TEXT("Keyboard: scanCode=%04x keyName=%s\r\n"), scanCode, keyNameBuffer);
        OutputDebugString(printBuffer);
    }
    ...

    return 0;
}
```

## -see-also

- [GetRawInputDeviceInfo](nf-winuser-getrawinputdeviceinfow.md)
- [RAWINPUT](ns-winuser-rawinput.md)
- [Raw Input](/windows/win32/inputdev/raw-input)
- [Keyboard and mouse HID client drivers](/windows-hardware/drivers/hid/keyboard-and-mouse-hid-client-drivers)
- [KEYBOARD_INPUT_DATA structure](../ntddkbd/ns-ntddkbd-keyboard_input_data.md)
- [Keyboard Input](/windows/desktop/inputdev/keyboard-input)
