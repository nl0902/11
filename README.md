import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Badge } from "@/components/ui/badge";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";

const benefits = [
  {
    title: "作品变现渠道",
    items: [
      "平台代理销售（商城、小程序、拍卖）",
      "线下空间驻展合作（酒店、茶馆、文旅）",
      "定制字画交易客户对接",
      "数字藏品发行支持（NFT）",
    ],
  },
  {
    title: "个人品牌商业包装",
    items: [
      "艺术家IP打造（宣传片/文案/名片）",
      "个人商城与销售页搭建",
      "媒体曝光与成交案例推广",
    ],
  },
  {
    title: "商业项目合作",
    items: [
      "书画+空间商业项目联营",
      "企业活动书画服务分发",
      "客户资源共享与项目撮合",
    ],
  },
  {
    title: "收益增长机制",
    items: [
      "推荐返佣体系",
      "年度激励奖项（商业之星）",
      "会员等级晋升制度",
    ],
  },
  {
    title: "商业能力提升",
    items: [
      "变现逻辑训练营",
      "书画直播变现指导",
      "税务/合同/版权实操培训",
    ],
  },
];

export default function ShuhuayuanSite() {
  return (
    <div className="p-6 max-w-6xl mx-auto">
      <h1 className="text-4xl font-bold mb-4 text-center">书画院商业联盟会员中心</h1>
      <p className="text-center text-lg text-gray-600 mb-8">
        为书画艺术家打造系统化商业赋能平台，助力作品变现、品牌打造与高端资源链接。
      </p>

      <Tabs defaultValue="benefits" className="mb-10">
        <TabsList className="flex flex-wrap justify-center gap-2">
          {benefits.map((section, index) => (
            <TabsTrigger key={index} value={section.title}>
              {section.title}
            </TabsTrigger>
          ))}
        </TabsList>
        {benefits.map((section, index) => (
          <TabsContent key={index} value={section.title}>
            <div className="grid grid-cols-1 md:grid-cols-2 gap-4 mt-6">
              {section.items.map((item, idx) => (
                <Card key={idx} className="shadow-md border border-gray-200">
                  <CardContent className="p-4">
                    <p className="text-base font-medium">{item}</p>
                  </CardContent>
                </Card>
              ))}
            </div>
          </TabsContent>
        ))}
      </Tabs>

      <div className="text-center mt-12">
        <Button className="text-lg px-10 py-5 rounded-2xl bg-gradient-to-r from-yellow-400 to-red-500 text-white shadow-lg hover:scale-105 transition-transform">
          立即加入终身会员
        </Button>
        <p className="mt-3 text-sm text-gray-500">
          成为会员，开启你的书画商业化新纪元。专属权益即刻解锁。
        </p>
      </div>
    </div>
  );
}
